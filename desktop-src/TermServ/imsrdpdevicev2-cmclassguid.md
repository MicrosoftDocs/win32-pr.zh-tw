---
title: IMsRdpDeviceV2 CmClassGuid 屬性
description: 包含裝置的 configuration manager 安裝類別 GUID。
ms.assetid: 29ebe2ca-d669-4cc1-8cc1-33490fbb9497
ms.tgt_platform: multiple
keywords:
- CmClassGuid 屬性遠端桌面服務
- CmClassGuid 屬性遠端桌面服務，IMsRdpDeviceV2 介面
- IMsRdpDeviceV2 介面遠端桌面服務，CmClassGuid 屬性
topic_type:
- apiref
api_name:
- IMsRdpDeviceV2.CmClassGuid
- IMsRdpDeviceV2.get_CmClassGuid
api_location:
- MsTscAx.dll
api_type:
- COM
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 47a13a8ee706a1e6d2f512a9f6dca98928e3d8d9
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "106969135"
---
# <a name="imsrdpdevicev2cmclassguid-property"></a>IMsRdpDeviceV2：： CmClassGuid 屬性

包含裝置的 configuration manager 安裝類別 GUID。

這個屬性是唯讀的。

## <a name="syntax"></a>語法


```C++
HRESULT get_CmClassGuid(
  [out, retval] BSTR *pCmClassGuid
);
```



## <a name="property-value"></a>屬性值

裝置的 configuration manager 安裝類別 GUID。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 7 SP1<br/>                                                          |
| 最低支援的伺服器<br/> | Windows Server 2008 R2 包含 SP1<br/>                                             |
| 類型程式庫<br/>             | <dl> <dt>MsTscAx.dll</dt> </dl> |
| DLL<br/>                      | <dl> <dt>MsTscAx.dll</dt> </dl> |
| IID<br/>                      | IID \_ IMsRdpDeviceV2 定義為5fb94466-7661-42a8-98b7-01904c11668f<br/>      |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMsRdpDeviceV2**](imsrdpdevicev2.md)
</dt> </dl>

 

 





