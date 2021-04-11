---
description: 結構，用來識別要評估的主機和來源檔案。
ms.assetid: 547EF59E-7DE5-45E4-948F-109547FAAEE7
title: 'WLDP_HOST_INFORMATION 結構 (Wldp .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- WLDP_HOST_INFORMATION
api_type:
- HeaderDef
api_location:
- wldp.h
ms.openlocfilehash: ad20be7fa5887e42c09248d04e14f5ff8cffcd54
ms.sourcegitcommit: c7add10d695482e1ceb72d62b8a4ebd84ea050f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104025829"
---
# <a name="wldp_host_information-structure"></a>WLDP \_ 主機 \_ 資訊結構

結構，用來識別要評估的主機和來源檔案。

## <a name="syntax"></a>語法


```C++
typedef struct _WLDP_HOST_INFORMATION {
  DWORD        dwRevision;
  WLDP_HOST_ID dwHostId;
  PCWSTR       szSource;
  HANDLE       hSource;
} WLDP_HOST_INFORMATION, *PWLDP_HOST_INFORMATION;
```



## <a name="members"></a>成員

<dl> <dt>

**dwRevision**
</dt> <dd>

必須是 **WLDP \_ 主機 \_ 資訊 \_ 修訂**。

</dd> <dt>

**dwHostId**
</dt> <dd>

[**WLDP \_ 主機 \_ 識別碼**](wldp-host-id.md)中的列舉值，其描述主機識別碼。

</dd> <dt>

**szSource**
</dt> <dd>

副檔名為的完整路徑和腳本名稱。 若為 **WLDP \_ 主機 \_ 識別碼 \_ 全域** 或手動腳本執行，則為 Null。

</dd> <dt>

**hSource**
</dt> <dd>

除了名稱之外，呼叫端還可以指定用於驗證之檔案的控制碼。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅 Windows 8 桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2012 \[ desktop 應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl> |



 

 




