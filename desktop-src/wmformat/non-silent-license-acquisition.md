---
title: 取得非無訊息授權
description: 取得非無訊息授權
ms.assetid: 3b3fce53-9202-4e55-82d5-7c70ea833087
keywords:
- Windows Media Format SDK，非無訊息授權取得
- Windows Media Format SDK，授權
- 數位版權管理 (DRM) 、非無訊息授權取得
- DRM (數位版權管理) 、非無訊息授權取得
- 數位版權管理 (DRM) 、授權
- DRM (數位版權管理) 、授權
- DRM 用戶端擴充 Api、非無訊息授權取得
- 用戶端擴充 Api、非無訊息授權取得
- 取得非無訊息授權
- 授權，非無訊息授權取得
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: adb8d7c4865e74fd5ce383cff8317de905828afe
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104507428"
---
# <a name="non-silent-license-acquisition"></a>取得非無訊息授權

非無訊息授權取得可讓授權提供者透過網頁與終端使用者互動，作為授權取得程式中的中繼步驟。 為了回應嘗試存取受保護內容的使用者，而起始了非無訊息授權取得。

若要執行非無訊息授權取得，請使用下列步驟：

1.  呼叫 [**IWMDRMLicenseManagement：： AcquireLicense**](iwmdrmlicensemanagement-acquirelicense.md) 方法。 從受保護的檔案傳入 DRM 標頭作為 *bstrHeaderData* 參數。 在 *bstrActions* 參數中指定您希望授權授與的許可權。 最後，將 *dwFlags* 參數設定為 [WMDRM \_ 取得 \_ 授權 NONSILENT] \_ 。
2.  **IWMDRMLicenseManagement** 介面的陷阱事件。 當您收到 **MEWMDRMLicenseAcquisitionCompleted** 事件時，請呼叫 **IMFMediaEvent：： GetValue** 來取得其相關聯的值。 值的類型應該是 VT UNKNOWN，也就是 \_ **IUnknown** 介面的指標。
3.  針對步驟2中所抓取的 **IUnknown** 介面呼叫 **QueryInterface** 方法，以取得 [**IWMDRMNonSilentLicenseAquisition**](iwmdrmnonsilentlicenseaquisition.md)介面。
4.  呼叫 [**IWMDRMNonSilentLicenseAquisition：： GetChallenge**](iwmdrmnonsilentlicenseaquisition-getchallenge.md) 來取得授權挑戰。 如果您沒有授權伺服器的 URL，也請呼叫 [**IWMDRMNonSilentLicenseAquisition：： GetURL**](iwmdrmnonsilentlicenseaquisition-geturl.md) 。
5.  將挑戰傳送至 URL 所指定的網頁。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**取得授權**](acquiring-licenses.md)
</dt> <dt>

[**使用媒體基礎事件模型**](using-the-media-foundation-model.md)
</dt> </dl>

 

 




