---
description: 包含可識別介面卡的資訊。
ms.assetid: d0d59df9-c512-4d69-b0a0-7d87d7a380f6
title: 'D3DADAPTER_IDENTIFIER9 結構 (D3D9Types .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- D3DADAPTER_IDENTIFIER9
api_type:
- HeaderDef
api_location:
- D3D9Types.h
ms.openlocfilehash: 85401573956d29386b5ddabbd48711a7be140463
ms.sourcegitcommit: 7e4322a6ec1f964d5ad26e2e5e06cc8ce840030e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 07/01/2021
ms.locfileid: "113129967"
---
# <a name="d3dadapter_identifier9-structure"></a>D3DADAPTER \_ IDENTIFIER9 結構

包含可識別介面卡的資訊。

## <a name="syntax"></a>語法


```C++
typedef struct D3DADAPTER_IDENTIFIER9 {
  char          Driver[MAX_DEVICE_IDENTIFIER_STRING];
  char          Description[MAX_DEVICE_IDENTIFIER_STRING];
  char          DeviceName[32];
#ifdef _WIN32
  LARGE_INTEGER DriverVersion;
#else
  DWORD         DriverVersionLowPart;
  DWORD         DriverVersionHighPart;
#endif
  DWORD         VendorId;
  DWORD         DeviceId;
  DWORD         SubSysId;
  DWORD         Revision;
  GUID          DeviceIdentifier;
  DWORD         WHQLLevel;
} D3DADAPTER_IDENTIFIER9, *LPD3DADAPTER_IDENTIFIER9;
```



## <a name="members"></a>成員

<dl> <dt>

**驅動程式**
</dt> <dd>

類型： **char**

</dd> <dd>

用於呈現給使用者。 這不應該用來識別特定的驅動程式，因為許多不同的字串可能與來自不同廠商的相同裝置和驅動程式相關聯。

</dd> <dt>

**說明**
</dt> <dd>

類型： **char**

</dd> <dd>

用於呈現給使用者。

</dd> <dt>

**DeviceName**
</dt> <dd>

類型： **char**

</dd> <dd>

GDI 的裝置名稱。

</dd> <dt>

**DriverVersion**
</dt> <dd>

類型： **[**大型 \_ 整數**](/windows/win32/api/winnt/ns-winnt-large_integer-r1)**

</dd> <dd>

識別 Direct3D 驅動程式的版本。 在64位帶正負號的整數值上進行小於和大於比較是合法的。 但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。 相反地，您應該使用 DeviceIdentifier。 請參閱＜備註＞。

</dd> <dt>

**DriverVersionLowPart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

識別 Direct3D 驅動程式的版本。 針對64位帶正負號的整數值進行 < 和 > 比較是合法的。 但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。 相反地，您應該使用 DeviceIdentifier。 請參閱＜備註＞。

</dd> <dt>

**DriverVersionHighPart**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

識別 Direct3D 驅動程式的版本。 針對64位帶正負號的整數值進行 < 和 > 比較是合法的。 但是，如果您使用此元素來識別有問題的驅動程式，請務必小心。 相反地，您應該使用 DeviceIdentifier。 請參閱＜備註＞。

</dd> <dt>

**VendorId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

可以用來協助識別特定晶片集。 查詢此成員以識別製造商。 如果不明，此值可以是零。

</dd> <dt>

**DeviceId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

可以用來協助識別特定晶片集。 查詢此成員以識別晶片集的類型。 如果不明，此值可以是零。

</dd> <dt>

**SubSysId**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

可以用來協助識別特定晶片集。 查詢此成員以識別子系統，通常是特定的面板。 如果不明，此值可以是零。

</dd> <dt>

**修訂**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

可以用來協助識別特定晶片集。 查詢此成員以識別晶片集的修訂層級。 如果不明，此值可以是零。

</dd> <dt>

**DeviceIdentifier**
</dt> <dd>

類型： **[ **GUID**](guid.md)**

</dd> <dd>

可以查詢以檢查驅動程式和晶片集的變更。 此 GUID 是驅動程式和晶片集配對的唯一識別碼。 查詢此成員以追蹤驅動程式和晶片集的變更，以便為圖形子系統產生新的設定檔。 DeviceIdentifier 也可用來識別特定有問題的驅動程式。

</dd> <dt>

**WHQLLevel**
</dt> <dd>

類型： **[ **DWORD**](../winprog/windows-data-types.md)**

</dd> <dd>

用來判斷此驅動程式和裝置配對的 Windows 硬體品質實驗室 (WHQL) 驗證等級。 DWORD 是一種封裝日期結構，用來定義由驅動程式傳遞的最新 WHQL 測試的發行日期。 對此值執行 < 和 > 作業是合法的。 以下說明日期格式。



| Bits  |  描述                                             |
|-------|-----------------------------------------------|
| 31-16 | 年份，從1999向上的十進位數。 |
| 15-8  | 月份，介於1到12之間的十進位數。     |
| 7-0   | Day，介於1到31之間的十進位數。       |



 

也會使用下列值。



| 值    |  描述                                                     |
|-----|-------------------------------------------------------|
| 0   | 未通過認證。                                        |
| 1   | 經 WHQL 驗證，但沒有可用的日期資訊。 |



 

Direct3D 9 與 Direct3D 9Ex 之間的差異：

如果是在 Windows Vista、Windows Server 2008、Windows 7 和 Windows Server 2008 R2 上執行的 Direct3D9Ex (或更多目前的作業系統) ， [**IDirect3D9：： GetAdapterIdentifier**](/windows/win32/api/d3d9/nf-d3d9-idirect3d9-getadapteridentifier) 會為 WHQL 層級傳回1，而不會檢查驅動程式的狀態。

</dd> </dl>

## <a name="remarks"></a>備註

下列虛擬虛擬的範例說明在 DriverVersion、DriverVersionLowPart 和 DriverVersionHighPart 成員中編碼的版本格式。


```
Product = HIWORD(DriverVersion.HighPart)
Version = LOWORD(DriverVersion.HighPart)
SubVersion = HIWORD(DriverVersion.LowPart)
Build = LOWORD(DriverVersion.LowPart)
```



如需 HIWORD 宏、LOWORD 宏和大型整數結構的詳細資訊，請參閱 Platform SDK \_ 。

\_裝置 \_ 識別碼字串上限 \_ 是具有下列定義的常數。


```
#define MAX_DEVICE_IDENTIFIER_STRING        512
```



VendorId、DeviceId、SubSysId 和修訂成員可以串聯使用，以識別特定晶片集。 不過，請小心使用這些成員。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|----------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>D3D9Types。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[Direct3D 結構](dx9-graphics-reference-d3d-structures.md)
</dt> </dl>

 

 
