---
description: 在選取專案時，會呼叫預覽處理常式，以在視圖的讀取窗格中顯示檔案內容的輕量、豐富、唯讀預覽。 這樣做不會啟動檔案的相關聯應用程式。
ms.assetid: 166a4001-d237-44a4-a457-e320e995639c
title: 預覽處理常式和 Shell 預覽主機
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 993c6c8e7b15d9bfc24b5dd42352407a3a53c45b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104973352"
---
# <a name="preview-handlers-and-shell-preview-host"></a>預覽處理常式和 Shell 預覽主機

在選取專案時，會呼叫預覽處理常式，以在視圖的讀取窗格中顯示檔案內容的輕量、豐富、 *唯讀* 預覽。 這樣做不會啟動檔案的相關聯應用程式。

本主題將討論下列主題：

-   [預覽處理常式架構](#preview-handler-architecture)
-   [伺服器模型選項](#server-model-options)
-   [初始 化](#initialization)
-   [預覽處理常式資料流程](#preview-handler-data-flow)
-   [對預覽處理常式進行偵錯工具](#debugging-a-preview-handler)
-   [提供您自己的預覽處理常式流程](#providing-your-own-process-for-a-preview-handler)
-   [相關主題](#related-topics)

## <a name="preview-handler-architecture"></a>預覽處理常式架構

預覽處理常式是託管應用程式。 主機包含 Windows Vista 或 Microsoft Outlook 2007 中的 Windows 檔案總管。 主機會將 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 實作為預覽處理常式和主機之間的通訊方法。

預覽處理常式本身會執行這些介面：

-   [**IInitializeWithStream**](/windows/desktop/api/Propsys/nn-propsys-iinitializewithstream)
-   [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)
-   [**IOleWindow**](/windows/win32/api/oleidl/nn-oleidl-iolewindow)
-   [**IPreviewHandler**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandler)
-   [**IPreviewHandlerVisuals**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlervisuals) (選用) 

您的處理常式會透過其 [**IObjectWithSite**](/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite)來呼叫，它會傳回一個 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown) 指標，要求 [**IPreviewHandlerFrame**](/windows/win32/api/shobjidl_core/nn-shobjidl_core-ipreviewhandlerframe) 物件與主機互動。

## <a name="server-model-options"></a>伺服器模型選項

預覽處理常式一律會用盡進程。 有兩種方法可以執行這項操作：

1.  預覽處理常式可以建立為同進程伺服器，但會透過跨進程的代理主機來執行。 這是慣用的方法。 系統會在 Prevhost.exe 檔案中為此提供代理主機。 這個方法所建立的預覽處理常式與 Windows XP 上的 Outlook 2007 不相容。 不過，這些相同的處理常式適用于在 Windows Vista 上執行的 Windows 檔案總管和 Outlook 2007。
2.  預覽處理常式可以用 (COM) server 的本機組件物件模型來建立。 不建議您這麼做的原因有好幾種。 首先，執行同進程伺服器比較容易。 更重要的是，執行為內含式伺服器，可提供更好的控制處理常式物件存留期，以提供更好的清除和效率。

根據預設，預覽處理常式會基於安全性理由，在低完整性層級 (IL) 進程中執行。 您可以藉由在登錄中設定下列值，選擇性地停用做為低 IL 處理常式的執行。 但是，不建議這麼做。 系統最終可能會將系統設定為拒絕不是低 IL 的任何處理程式。

```
HKEY_CLASSES_ROOT
   CLSID
      {YOUR HANDLER'S CLSID}
         DisableLowILProcessIsolation [DWORD] = 1
```

依預設，不同的預覽處理常式會共用相同的進程。 Prevhost.exe 可以同時執行兩個實例;一個用於以低 IL 進程的形式執行的處理常式，一個用於已退出宣告該行為的處理常式。

## <a name="initialization"></a>初始化

如同縮圖和屬性處理常式，強烈建議您使用資料流程初始化處理常式。 如有必要，您可以透過檔案或專案初始化，但資料流程提供最安全的方式來執行處理常式。 透過資料流程進行初始化可確保檔案完整性和穩定性，讓執行處理常式的系統成為低 IL 進程，例如保護系統免于緩衝區溢位、限制處理常式可以寫入資訊的位置，以及限制與其他視窗的通訊。

如果您必須使用檔案或 Shell 專案來初始化，請儲存檔案路徑或 [**IShellItem**](/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellitem)的參考。 在呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 之前，請勿從這些來源讀取資料。

一般情況下，初始化不應執行任何繁重的工作，例如撰寫和儲存預覽影像。 為了達到最佳效率，在呼叫預覽之前，不應執行這類處理。

## <a name="preview-handler-data-flow"></a>預覽處理常式資料流程

預覽程式中的資料流程會遵循此處顯示的一般路徑。 您可以將主機視為 Windows Vista 或 Outlook 2007 中的 Windows 檔案總管。

1.  預覽處理常式已初始化，最好是使用資料流程。
2.  視圖視窗會透過 [**IPreviewHandler：： SetWindow**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setwindow)從主機傳遞給處理常式。
3.  此時，處理常式應該不會再執行任何動作，直到 [**IPreviewHandler：呼叫:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview) 為止。
4.  預覽會透過呼叫 [**IPreviewHandler：:D opreview**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-dopreview)顯示在 [讀取窗格] 中。
5.  視窗的大小是透過 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)來設定。
6.  視窗會在需要時透過 [**IPreviewHandler：： SetRect**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-setrect)調整大小。
7.  您可以透過呼叫 [**IPreviewHandler：： Unload**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ipreviewhandler-unload)，卸載預覽並在不再需要時釋放其資源。

## <a name="debugging-a-preview-handler"></a>對預覽處理常式進行偵錯工具

如果您已遵循將預覽處理常式實作為同進程伺服器的建議，以將您的預覽處理常式進行偵錯工具，您可以將其附加至 Prevhost.exe。 如先前所述，請注意，Prevhost.exe 的兩個實例，一個用於一般的低 IL 進程，另一個用於已選擇不以低 IL 進程的方式執行的處理常式。

如果您在可用的進程清單中找不到 Prevhost.exe，表示該時間點可能尚未載入。 按一下檔案以供預覽時，會載入代理程式，然後應該會顯示為可附加的進程。

## <a name="providing-your-own-process-for-a-preview-handler"></a>提供您自己的預覽處理常式流程

如果您想要強制建立處理常式的新進程，而不是在預設進程下執行，請為您的處理常式在 **AppID** 下建立新的子機碼，並將其 DllSurrogate 專案設定為 "Prevhost.exe"。 使用 **appid** 子機碼，而不是預設的 Prevhost.exe **appid**。

藉由提供新的處理常式，處理常式可以避免在共用進程下執行，如同預設的一樣。 例如，這可以讓您確保特定版本的 common language runtime (CLR) 在進程中。 如果您要建立預覽處理常式的 managed 執行，則這是必要的。

> [!Note]  
> 32位預覽處理常式在64位作業系統上安裝時，應使用 **AppID** {534A1E02-D58F-44f0-B58B-36CBED287C7C}。

 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立預覽處理常式](building-preview-handlers.md)
</dt> <dt>

[如何註冊預覽處理常式](how-to-register-a-preview-handler.md)
</dt> <dt>

[預覽處理常式指導方針](preview-handler-guidelines.md)
</dt> </dl>

 

 
