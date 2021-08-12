---
description: 通知 DWM 內送更新至視窗共用介面。
ms.assetid: 8357D977-E501-47D7-85BC-7C8954C6D166
title: DwmDxUpdateWindowSharedSurface 函式
ms.topic: reference
ms.date: 11/27/2018
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- Dwmapi.dll
api_name:
- DwmDxUpdateWindowSharedSurface
ms.openlocfilehash: 9eac390cd6ccf79ed3f916f4c9605b938ab9fd338df3643301d7f5e5c900c0d7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118280118"
---
# <a name="dwmdxupdatewindowsharedsurface-function"></a>DwmDxUpdateWindowSharedSurface 函式

通知 DWM 內送更新至視窗共用介面。

## <a name="syntax"></a>語法

```C++
HRESULT WINAPI DwmDxUpdateWindowSharedSurface(
  _In_     HWND     hwnd,
  _In_     UINT64   uiUpdateId,
  _In_     DWORD    dwFlags,
  _In_opt_ HMONITOR hmonitorAssociation,
  _In_     RECT     *prc
);
```

## <a name="parameters"></a>參數

`hwnd`

指定要更新之視窗的 [**HWND**](/windows/desktop/winprog/windows-data-types) 。

`uiUpdateId`

從 [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md)中取出的更新識別碼。

`dwFlags`

保留的。

`hmonitorAssociation`

保留的。

`prc`

要更新之視窗的矩形（在視窗座標空間中）。 Null 矩形表示未更新任何區域。

## <a name="return-value"></a>傳回值

**S \_** 如果成功，則為 [確定]，否則為失敗的 **HRESULT。**

## <a name="remarks"></a>備註

此 API 適用于執行圖形驅動程式或執行時間。 應用程式可能不會呼叫這個方法。 本檔僅適用于 Windows 7，此 API 不保證存在，也不會在其他版本的 Windows 上以類似的方式運作。 此函式不會出現在任何標頭或靜態程式庫中，而且位於 dwmapi.dll 的序數101。

只有在 [**DwmDxGetWindowSharedSurface**](dwmdxgetwindowsharedsurface.md) 傳回 **S \_ OK** 之後，才應該呼叫這個方法，而且必須在該情況下呼叫，不論介面是否更新。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | 僅 Windows 7 \[ 桌面應用程式\] |
| 最低支援的伺服器 | 都不支援 |
| 用戶端支援結束 | Windows 7 |
| 標頭 | N/A |
| DLL | Dwmapi.dll |
