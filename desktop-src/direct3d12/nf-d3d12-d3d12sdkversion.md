---
title: D3D12SDKVersion 符號
description: Direct3D 12 SDK 版本號碼。
ms.localizationpriority: low
ms.topic: reference
ms.date: 08/25/2021
req.lib: ''
req.dll: d3d12core.dll
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- d3d12core.dll
api_name:
- D3D12SDKVersion
targetos: Windows
ms.openlocfilehash: 0bf0aa17e16a4274b69e80580c0615ed055dd97a
ms.sourcegitcommit: 61a4c522182aa1cacbf5669683d9570a3bf043b2
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122917890"
---
# <a name="d3d12sdkversion-symbol"></a>D3D12SDKVersion 符號

Direct3D 12 SDK 版本號碼。

## <a name="syntax"></a>語法

```cpp
extern "C" { _declspec(dllexport) extern const UINT D3D12SDKVersion = n;}
```

## <a name="return-value"></a>傳回值

包含 Direct3D 12 SDK 版本號碼的 [UINT](/windows/win32/winprog/windows-data-types) 。

## <a name="remarks"></a>備註

**D3D12SDKVersion** 不會與匯入程式庫和標頭檔相關聯。

## <a name="requirements"></a>規格需求

| &nbsp; | &nbsp; |
| ---- |:---- |
| **目標平台** | Windows |
| **標頭** | N/A |
| **程式庫** | N/A |
| **DLL** | d3d12core.dll |

## <a name="see-also"></a>另請參閱
