---
title: In-Context 攔截函式的預防措施
description: 基於效能考慮，用戶端開發人員會註冊內容攔截函式。
ms.assetid: 14b48920-a291-4519-b005-e559263a0e83
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c0e319037cb1295725548b3361bf076b4b1f760
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "106965661"
---
# <a name="in-context-hook-function-precautions"></a>In-Context 攔截函式的預防措施

基於效能考慮，用戶端開發人員會註冊內容攔截函式。 不過，由於這些攔截函式會對應到伺服器的位址空間，因此用戶端和伺服器開發人員必須採取預防措施，以確保事件處理順利進行。

## <a name="precautions-for-client-developers"></a>用戶端開發人員的預防措施

用戶端開發人員應留意下列問題：

-   內容攔截函式不應該使用大量的處理器時間，因為攔截函式必須在伺服器應用程式繼續之前傳回。
-   觸發事件之後，呼叫攔截函式時，與事件相關聯的視窗就可能不再存在。 用戶端必須先確認與事件相關聯的視窗仍然存在，再採取任何其他與事件相關的動作。 為了確保視窗仍然存在，用戶端會使用 Microsoft Win32 [**IsWindow**](/windows/desktop/api/winuser/nf-winuser-iswindow) 函數。
-   如果已定義攔截函式的 DLL 連結至另一個 DLL，用戶端開發人員必須確保系統載入另一個 DLL。 如果使用 .def 檔隱含連結 (並匯入) ，則額外的 DLL 必須位於 Windows 目錄或其中一個系統目錄（例如 Windows \\ system、windows \\ System32 或 windows SysWOW64）中 \\ 。 如果使用 [**LoadLibrary**](/windows/desktop/api/libloaderapi/nf-libloaderapi-loadlibrarya)) 明確地連結 (，則必須在 **LoadLibrary** 的呼叫中指定其他 DLL 所在目錄的完整路徑。
-   當包含攔截函式的 DLL 載入至16位應用程式時，內容中攔截函式可能會造成堆疊溢位。 發生此問題的原因是，16位應用程式使用的固定堆疊大小不夠大，無法容納會導致呼叫攔截函式的系統函數調用鏈。

## <a name="precautions-for-server-developers"></a>伺服器開發人員的預防措施

伺服器開發人員必須注意，用戶端應用程式可能會註冊內容攔截函式。 當伺服器呼叫 [**NotifyWinEvent**](/windows/desktop/api/Winuser/nf-winuser-notifywinevent)時，必須做好準備以處理 [**WM \_ GETOBJECT**](wm-getobject.md) 和其他 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 方法。

## <a name="invalid-interface-pointers"></a>不正確介面指標

當用戶端在內容攔截函式內呼叫 [**AccessibleObjectFromEvent**](/windows/desktop/api/Oleacc/nf-oleacc-accessibleobjectfromevent) 時，傳回的 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 介面指標會直接指向伺服器位址空間中的程式碼。 如果用戶端使用這個指標呼叫介面屬性，則元件物件模型 (COM) 程式庫不涉及封送處理 (封裝和傳送跨進程界限的介面參數) 或封送處理跨進程界限傳送的 (解除封裝參數，而不會偵測物件是否終結。

如果用戶端呼叫介面屬性至已終結的物件，則不正確介面指標會在伺服器的位址空間中造成一般保護錯誤，除非伺服器偵測到這種情況。

為了防止不正確介面指標，伺服器會建立可包裝可存取物件的 [proxy 物件](creating-proxy-objects.md) ，並監視可存取物件的存留期範圍。 例如，當用戶端呼叫 [**IAccessible**](/windows/desktop/api/oleacc/nn-oleacc-iaccessible) 屬性來取得物件的相關資訊時，proxy 會檢查可存取的物件是否仍然可用，如果是，則會將用戶端的要求轉送至可存取的物件。 如果可存取物件已損毀，則 proxy 會將錯誤傳回給用戶端。

 

 