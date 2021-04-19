---
title: WMDMID 結構
description: WMDMID 結構描述序號和群組識別碼。
ms.assetid: eaa5786e-a2a1-42d7-b527-be83d944cb20
keywords:
- WMDMID 結構 windows Media 裝置管理員
- PWMDMID 結構指標 windows Media 裝置管理員
topic_type:
- apiref
api_name:
- WMDMID
api_location:
- wmdm.idl
api_type:
- HeaderDef
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8edc2a364bf29ead6aaf4fad8ad3a56fe80d7176
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "107001191"
---
# <a name="wmdmid-structure"></a>WMDMID 結構

**WMDMID** 結構描述序號和群組識別碼。

## <a name="syntax"></a>語法


```C++
typedef struct __WMDMID {
  UINT  cbSize;
  DWORD dwVendorID;
  BYTE  pID[WMDMID_LENGTH];
  UINT  SerialNumberLength;
} WMDMID, *PWMDMID;
```



## <a name="members"></a>成員

<dl> <dt>

**cbSize**
</dt> <dd>

**WMDMID** 結構的大小（以位元組為單位）。

</dd> <dt>

**dwVendorID**
</dt> <dd>

**DWORD** ，包含廠商的註冊 ID 號碼。 如果不在使用中，則包含零。

</dd> <dt>

**pID \[ WMDMID \_ 長度\]**
</dt> <dd>

包含序號之位元組陣列的指標。 序號是沒有標準格式的位元組值字串。 請注意，這不是寬字元的值。 **WMDMID \_長度** 是在 mswmdm 中定義的常數值。

</dd> <dt>

**SerialNumberLength**
</dt> <dd>

傳回之序號的實際長度（以位元組為單位）。

</dd> </dl>

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|-------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Wmdm .idl</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IMDSPDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspdevice-getserialnumber)
</dt> <dt>

[**IMDSPStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-imdspstorageglobals-getserialnumber)
</dt> <dt>

[**IWMDMDevice::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmdevice-getserialnumber)
</dt> <dt>

[**IWMDMStorageGlobals::GetSerialNumber**](/windows/desktop/api/mswmdm/nf-mswmdm-iwmdmstorageglobals-getserialnumber)
</dt> <dt>

[**結構**](structures.md)
</dt> </dl>

 

 





