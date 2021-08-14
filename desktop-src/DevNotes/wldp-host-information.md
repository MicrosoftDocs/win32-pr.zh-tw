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
ms.openlocfilehash: cc1bed8fd104b4aa6abb83d3eb7e19faa37a0301429312c8f0799e256ce32ec6
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118404067"
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
| 最低支援的用戶端<br/> | Windows 8 \[僅限桌面應用程式\]<br/>                                        |
| 最低支援的伺服器<br/> | Windows Server 2012 \[僅限桌面應用程式\]<br/>                              |
| 標頭<br/>                   | <dl> <dt>Wldp。h</dt> </dl> |



 

 




