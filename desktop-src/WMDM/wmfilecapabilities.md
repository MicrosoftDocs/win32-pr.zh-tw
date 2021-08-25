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
ms.openlocfilehash: a4f4852eeb7142b92c2c1a4c2073dfc70e5f6a6d74c727a7ab9e63c285796846
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119903768"
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

 

 





