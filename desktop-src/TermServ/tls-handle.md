---
title: TLS_HANDLE
description: 代表遠端桌面授權伺服器的控制碼。
ms.assetid: 6da51660-a9fd-4e49-97e3-ba0829b1bbbf
ms.tgt_platform: multiple
keywords:
- TLS_HANDLE
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 04daf14429a5b400267e664a615739fd14e8306e987f50726cfdb341522870a2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119869448"
---
# <a name="tls_handle"></a>TLS \_ 控制碼

代表遠端桌面授權伺服器的控制碼。 [**TLSConnectToLsServer**](tlsconnecttolsserver.md)函數會傳回這個控制碼。

> [!Note]  
> 此資料類型沒有相關聯的標頭檔。 若要使用它，您必須自行定義，如本主題所示。

 


```C++
typedef HANDLE TLS_HANDLE;
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|--------------------------------|
| 最低支援的用戶端<br/> | Windows Vista<br/>       |
| 最低支援的伺服器<br/> | Windows Server 2008<br/> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**TLSConnectToLsServer**](tlsconnecttolsserver.md)
</dt> <dt>

[**TLSDisconnectFromServer**](tlsdisconnectfromserver.md)
</dt> </dl>

 

 





