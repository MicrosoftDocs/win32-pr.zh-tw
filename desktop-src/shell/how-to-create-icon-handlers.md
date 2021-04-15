---
description: 說明如何建立自訂圖示指派的處理常式。
ms.assetid: 23ed3a21-cf62-4440-b983-fae23aa56890
title: 如何建立圖示處理常式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e2c620b6f6a4c05f8996a26c8365e4f4201ee0b4
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104973172"
---
# <a name="how-to-create-icon-handlers"></a>如何建立圖示處理常式

[檔案類型](fa-file-types.md)通常有與其相關聯的自訂圖示，可讓其成員在 Windows 檔案總管中容易辨識。 將自訂圖示指派給檔案類型最簡單的方式，就是註冊圖示的檔案。 不過，以這種方式註冊的圖示在檔案類型的所有成員中都是相同的。 您可以藉由執行 *圖示處理常式*，在將圖示指派給檔案類型的成員時，有更多的彈性。

圖示處理常式是一種 Shell 延伸模組處理常式，可讓您以動態方式將圖示指派給檔案類型的成員。 每次顯示類型的檔案時，Shell 會查詢適當圖示的處理常式。 例如，圖示處理常式可以將不同的圖示指派給檔案類型的不同成員，或根據檔案的目前狀態來改變圖示。

[建立 shell](handlers.md)擴充處理常式時，會討論如何執行和註冊 shell 擴充處理常式的一般程式。 本檔著重于圖示處理常式特定的執行層面。

-   [執行圖示處理常式](#step-1-implementing-icon-handlers)
-   [執行 IExtractIcon 介面](#step-2-implementing-the-iextracticon-interface)
-   [註冊圖示處理常式](#step-3-registering-icon-handlers)
-   [相關主題](#related-topics)

## <a name="instructions"></a>指示

### <a name="step-1-implementing-icon-handlers"></a>步驟1：執行圖示處理常式

就像所有 Shell 擴充處理常式一樣，圖示處理常式也是實作為 Dll (COM) 物件的同進程元件物件模型。 除了 [**IUnknown**](/windows/win32/api/unknwn/nn-unknwn-iunknown)： [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 和 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)之外，它們還必須匯出兩個介面。

Shell 會透過其 [**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile) 介面初始化處理常式。 它會使用此介面來要求 (CLSID) 的處理常式類別識別碼，並提供該檔案的名稱。 其餘的作業會透過 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) 介面進行。 如需如何執行 Shell 延伸模組處理常式（包括 **IPersistFile** 介面）的一般討論，請參閱 [建立 shell 擴充處理](handlers.md)程式。 本檔的其餘部分將討論如何執行 **IExtractIcon** 介面。

### <a name="step-2-implementing-the-iextracticon-interface"></a>步驟2：執行 IExtractIcon 介面

初始化介面之後，Shell 會使用處理程式的 [**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona) 介面來要求適當的圖示。 介面有兩種方法： [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) 和 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)。

圖示是由其在檔案系統中的位置來識別。 呼叫 [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation) 方法以要求這項資訊。 將 *szIconFile* 參數設定為檔案名。 如果檔案中有一個以上的圖示，請將 *piIndex* 設定為圖示的索引。 為兩個旗標變數指派適當的值。 如果您不想要指定檔案名，或不想要讓 Shell 將圖示解壓縮，請在 *pwFlags* 參數中設定 **GIL \_ NOTFILENAME** 旗標。 您不需要指派值給 *szIconFile*，不過當 Shell 呼叫 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)時，處理常式必須提供圖示控制碼。

如果您傳回檔案名，Shell 通常會嘗試從其快取載入圖示。 若要防止載入快取的圖示，請在 *pwFlags* 參數中設定 **GIL \_ DONTCACHE** 旗標。 如果未載入快取的圖示，則 Shell 會呼叫 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract) 以要求圖示控制碼。

如果檔案和索引是由 [**IExtractIcon：： GetIconLocation**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-geticonlocation)指定，它們會分別傳遞給 *pszFile* 和 *nIconIndex* 參數中的 [**IExtractIcon：：解壓縮**](/windows/win32/api/shlobj_core/nf-shlobj_core-iextracticona-extract)。 如果有提供檔案名，您的處理常式可以傳回 \_ FALSE，讓 Shell 將圖示解壓縮。 否則，您的處理常式必須解壓縮或產生大型和小型圖示，並將其 HICON 控制碼指派給 *phiconLarge* 和 *phiconSmall* 參數。 Shell 會將圖示新增至其快取，以加速後續呼叫處理常式。

### <a name="step-3-registering-icon-handlers"></a>步驟3：註冊圖示處理常式

當您以 [靜態方式註冊](icon.md)[檔案類型](fa-file-types.md)的圖示時，會在檔案類型的 ProgID 底下建立 **DefaultIcon** 子機碼。 其預設值會設定為包含圖示的檔案。 若要註冊圖示處理常式，您仍然必須有 **DefaultIcon** 子機碼，但其預設值必須設定為 "%1"。 將 **IconHandler** 子機碼新增至 ProgID 子機碼的 **Shellex** 子機碼，並將其預設值設定為處理常式 CLSID GUID 的字串形式。 如需如何註冊 Shell 擴充處理常式的一般討論，請參閱 [建立 Shell 擴充處理](handlers.md)程式。

下列範例會從 [自訂圖示](icon.md) 修改登錄專案，讓 myp 檔案類型現在使用快捷方式功能表處理常式，而不是靜態定義的圖示。

```
HKEY_CLASSES_ROOT
   .myp
      (Default) = MyProgram.1
   MyProgram.1
      (Default) = MyProgram Application
      DefaultIcon
         (Default) = %1
      Shellex
         IconHandler
            (Default) = {The handler's CLSID GUID}
```

## <a name="related-topics"></a>相關主題

<dl> <dt>

[建立 Shell 擴充功能處理常式](handlers.md)
</dt> <dt>

[**IPersistFile**](/windows/win32/api/objidl/nn-objidl-ipersistfile)
</dt> <dt>

[**IExtractIcon**](/windows/win32/api/shlobj_core/nn-shlobj_core-iextracticona)
</dt> </dl>

 

 
