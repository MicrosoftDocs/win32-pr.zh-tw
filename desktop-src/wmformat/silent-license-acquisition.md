---
title: 無訊息授權取得
description: 無訊息授權取得
ms.assetid: bf88f1bb-0cbb-4c30-92e0-3d342977d67f
keywords:
- Windows媒體格式 SDK，無提示授權取得
- Windows媒體格式 SDK，授權
- 數位版權管理 (DRM) ，無訊息授權取得
- DRM (數位版權管理) ，無訊息授權取得
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api，無提示授權取得
- 用戶端擴充 Api，取得無訊息授權
- 無訊息授權取得
- 授權，取得無訊息授權
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7eff454ce673230f0c7dbe6f64afbf46e9bbe8b5f948609f5fb67d647a4151ca
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118197460"
---
# <a name="silent-license-acquisition"></a>無訊息授權取得

無訊息授權取得只需要單一方法呼叫，就能以非同步方式處理授權伺服器的所有網路通訊。

這種授權取得通常是用來回應嘗試存取受保護內容的使用者，例如，嘗試在 media player 應用程式中播放受保護的檔案。 因為無訊息授權取得會取得具有單一呼叫的授權，所以如果需要來自使用者的額外輸入（例如內容的付款），就不能使用它。

若要執行無訊息授權取得，請使用下列步驟：

1.  呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 方法。 從受保護的檔案傳入 DRM 標頭作為 *bstrHeaderData* 參數。 在 *bstrActions* 參數中指定您希望授權授與的許可權。 最後，將 *dwFlags* 參數設定為 WMDRM \_ 取得 \_ 授權 \_ 無訊息。
2.  [**IWMDRMLicenseManagement**](iwmdrmlicensemanagement.md)介面的陷阱事件。 當您收到 **MEWMDRMLicenseAcquisitionCompleted** 事件時，請呼叫 **IMFMediaEvent：： GetStatus** 方法（記載于媒體基礎檔中）來檢查其傳回碼。 如果取出的 **HRESULT** 值是成功的程式碼，則表示授權已成功下載，且位於本機授權存放區，可供使用。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**取得授權**](acquiring-licenses.md)
</dt> <dt>

[**使用媒體基礎事件模型**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




