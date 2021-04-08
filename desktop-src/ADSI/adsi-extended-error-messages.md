---
title: ADSI 擴充的錯誤訊息
description: 本主題包含一份主題清單，說明如何使用 IADs、IADsContainer、IDirectoryObject 和 >idirectorysearch 所傳回的 ADSI 錯誤訊息。
ms.assetid: cfec86cb-fe90-4e2b-8c9d-06e175253fa4
ms.tgt_platform: multiple
keywords:
- ADSI 擴充的錯誤訊息
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ab374f18892c0ff336ef588dce477db60405ab19
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104020815"
---
# <a name="adsi-extended-error-messages"></a>ADSI 擴充的錯誤訊息

除了 **HRESULT** 值之外，數個 ADSI 系統提供者 (大多是 LDAP) 為下列介面所執行的作業傳回其他錯誤資料：

-   [**IADs**](/windows/desktop/api/Iads/nn-iads-iads)
-   [**IADsContainer**](/windows/desktop/api/Iads/nn-iads-iadscontainer)
-   [**IDirectoryObject**](/windows/desktop/api/Iads/nn-iads-idirectoryobject)
-   [**>idirectorysearch**](/windows/desktop/api/Iads/nn-iads-idirectorysearch)

這類擴充錯誤資料的一部分是伺服器在訊息結果中傳送的字串。

呼叫 [**ADsGetLastError**](/windows/desktop/api/Adshlp/nf-adshlp-adsgetlasterror) 以取出這類的擴充錯誤訊息。 這個函式（ *lpError*）的第一個參數是 **DWORD** 值。 針對 Active Directory 伺服器，ADSI 會嘗試將 LDAP 錯誤訊息對應到適當的 Win32 錯誤碼，並將 Win32 錯誤碼值指派給 *lpError*。 無法解析對應，ADSI 會將 **錯誤的 \_ 無效 \_ 資料** 指派給 *lpError*，如同任何其他目錄伺服器一樣。 在所有情況下，ADSI 會透過 *lpErrorBuf*（ **ADsGetLastError** 函數的第二個參數），將錯誤描述的字串從伺服器轉送到用戶端。

 

 




