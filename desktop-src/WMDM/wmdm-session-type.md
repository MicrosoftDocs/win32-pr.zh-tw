---
title: WMDM_SESSION_TYPE 列舉
description: WMDM \_ 會話 \_ 類型列舉型別會定義會話類型。
ms.assetid: e4ed41c0-521f-4da0-8361-287b64d74d77
keywords:
- WMDM_SESSION_TYPE 列舉 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDM_SESSION_TYPE
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 84322986266143e5ff4ecc469c56504f29de9e3a
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106977623"
---
# <a name="wmdm_session_type-enumeration"></a>WMDM \_ 會話 \_ 類型列舉

**WMDM \_ 會話 \_ 類型** 列舉型別會定義會話類型。

## <a name="syntax"></a>Syntax


```C++
typedef enum tagWMDM_SESSION_TYPE { 
  WMDM_SESSION_NONE,
  WMDM_SESSION_TRANSFER_TO_DEVICE,
  WMDM_SESSION_TRANSFER_FROM_DEVICE,
  WMDM_SESSION_DELETE,
  WMDM_SESSION_CUSTOM
} WMDM_SESSION_TYPE;
```



## <a name="constants"></a>常數

<dl> <dt>

<span id="WMDM_SESSION_NONE"></span><span id="wmdm_session_none"></span>**WMDM \_ 會話 \_ 無**
</dt> <dd>

未定義會話。

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_TO_DEVICE"></span><span id="wmdm_session_transfer_to_device"></span>**WMDM \_ 會話 \_ 傳送 \_ 至 \_ 裝置**
</dt> <dd>

此會話定義為將資料傳送至裝置。

</dd> <dt>

<span id="WMDM_SESSION_TRANSFER_FROM_DEVICE"></span><span id="wmdm_session_transfer_from_device"></span>**\_ \_ \_ 從裝置 WMDM 會話 \_ 傳送**
</dt> <dd>

此會話定義為從裝置傳送資料。

</dd> <dt>

<span id="WMDM_SESSION_DELETE"></span><span id="wmdm_session_delete"></span>**WMDM \_ 會話 \_ 刪除**
</dt> <dd>

此會話定義為刪除資料。

</dd> <dt>

<span id="WMDM_SESSION_CUSTOM"></span><span id="wmdm_session_custom"></span>**WMDM \_ 會話 \_ 自訂**
</dt> <dd>

此會話定義為自訂會話。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**列舉類型**](enumeration-types.md)
</dt> </dl>

 

 





