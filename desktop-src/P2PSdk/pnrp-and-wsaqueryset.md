---
description: PNRP 會使用 WSAQUERYSET 結構搭配各種函式，以加速解析名稱和列舉名稱和雲端。
ms.assetid: 0ccf20c1-4c95-4caf-a8f3-82a9e0a9907b
title: 'PNRP 和 WSAQUERYSET (P2P. h) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 7d09d135d57af0922feb5a143c41696d85dac083
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106998306"
---
# <a name="pnrp-and-wsaqueryset"></a>PNRP 和 WSAQUERYSET

PNRP 會使用 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 結構搭配各種函式，以加速解析名稱和列舉名稱和雲端。

如需 [**WSAQUERYSET**](winsock-nsp-reference-links.md) 或 Windows 通訊端函式的完整定義，請參閱其在 Platform SDK 的 Windows 通訊端 2 API 檔中各自的定義。

## <a name="wsaqueryset-and-wsasetservice"></a>WSAQUERYSET 和 WSASetService

[**WSASetService**](winsock-nsp-reference-links.md)函數會使用 **WSAQUERYSET** 結構來註冊或移除對等名稱。 [PNRP 和 WSASetService](pnrp-and-wsasetservice.md)頁面概述如何搭配使用 **WSAQUERYSET** 結構與此函數。

## <a name="wsaqueryset-and-wsalookupservicebegin"></a>WSAQUERYSET 和 WSALookupServiceBegin

[**WSAQUERYSET**](winsock-nsp-reference-links.md)結構廣泛用於 **WSALookupServiceBegin**、 **WSALookupServiceNext** 和 **WSALookupServiceEnd** 函數。 下列參考頁面詳細說明這些函數如何使用 **WSAQUERYSET** 結構：

-   [PNRP 和 WSALookupServiceBegin](pnrp-and-wsalookupservicebegin.md)
-   [PNRP 和 WSALookupServiceNext](pnrp-and-wsalookupservicenext.md)
-   [PNRP 和 WSALookupServiceEnd](pnrp-and-wsalookupserviceend.md)

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 Windows XP （含 SP2） \[ 桌面應用程式\]<br/>                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2008 \[ desktop 應用程式\]<br/>                             |
| 版本<br/>                  | Windows XP （含 SP1）與 Windows XP 的 Advanced 網路套件<br/>  |
| 標頭<br/>                   | <dl> <dt>P2P。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[PNRP 和 BLOB](pnrp-and-blob.md)
</dt> <dt>

[PNRP 和 WSASetService](pnrp-and-wsasetservice.md)
</dt> </dl>

 

 




