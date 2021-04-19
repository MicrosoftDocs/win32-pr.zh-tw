---
title: WMFILECAPABILITIES 結構
description: WMFILECAPABILITIES 結構描述 MIME 型別。
ms.assetid: 30307343-f55e-4695-9ae8-b938617d749d
keywords:
- WMFILECAPABILITIES 結構 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMFILECAPABILITIES
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cc7657ddd15a4219a0d5f56dbadeffba2a9547bf
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106975955"
---
# <a name="wmfilecapabilities-structure"></a>WMFILECAPABILITIES 結構

**WMFILECAPABILITIES** 結構描述 MIME 型別。

## <a name="syntax"></a>語法


```C++
typedef struct _tagWMFILECAPABILITIES {
  LPWSTR pwszMimeType;
  DWORD  dwReserved;
} WMFILECAPABILITIES;
```



## <a name="members"></a>成員

<dl> <dt>

**pwszMimeType**
</dt> <dd>

MIME 類型。

</dd> <dt>

**>dwreserved**
</dt> <dd>

**DWORD** 保留供日後使用。 設定為零 (0) 。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IWMDMDevice2::GetFormatSupport2**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice2-getformatsupport2)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





