---
title: 'Win32_RDSHServer 類別的 GetInt32Property 方法 (appanalysis .h) '
description: 抓取 Win32 RDSHServer 物件的整數屬性值 \_ 。
ms.assetid: 4601e9cb-927b-4af8-a12b-09a8ca44c2f7
ms.tgt_platform: multiple
keywords:
- GetInt32Property 方法遠端桌面服務
- GetInt32Property 方法遠端桌面服務，Win32_RDSHServer 類別
- Win32_RDSHServer 類別遠端桌面服務，GetInt32Property 方法
topic_type:
- apiref
api_name:
- Win32_RDSHServer.GetInt32Property
api_location:
- RDMS.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 29a2427cfa19a84a8b8988cceacf3e0b836a031f
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103934587"
---
# <a name="getint32property-method-of-the-win32_rdshserver-class"></a>Win32 RDSHServer 類別的 GetInt32Property 方法 \_

抓取 [**Win32 \_ RDSHServer**](win32-rdshserver.md) 物件的整數屬性值。

## <a name="syntax"></a>語法


```mof
uint32 GetInt32Property(
  [in]  string Key,
  [out] sint32 Value
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*金鑰* \[在\]
</dt> <dd>

識別要取得之屬性的索引鍵。

</dd> <dt>

*值* \[擴展\]
</dt> <dd>

接收已抓取的屬性值。

</dd> </dl>

## <a name="return-value"></a>傳回值

成功時傳回0，否則會傳回 WMI 錯誤碼。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 都不支援<br/>                                                                                      |
| 最低支援的伺服器<br/> | Windows Server 2012<br/>                                                                                 |
| 命名空間<br/>                | 根 \\ CIMv2 \\ rdm<br/>                                                                                   |
| 標頭<br/>                   | <dl> <dt>Appanalysis。h</dt> </dl> |
| MOF<br/>                      | <dl> <dt>RDManagement mof</dt> </dl>                    |
| DLL<br/>                      | <dl> <dt>RDMS.dll</dt> </dl>                            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**Win32 \_ RDSHServer**](win32-rdshserver.md)
</dt> </dl>

 

 





