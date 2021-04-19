---
description: 抓取支援指定視窗的 DirectX 共用介面。 您可以將這個介面寫入，以便更新視窗的內容。
ms.assetid: 500CF5B4-0D56-4201-91F4-7333E45DACEE
title: DwmDxGetWindowSharedSurface 函式
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
- DwmDxGetWindowSharedSurface
ms.openlocfilehash: 15e7829383ce23e5bc06bb61ab9c0c224ab18182
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106969258"
---
# <a name="dwmdxgetwindowsharedsurface-function"></a>DwmDxGetWindowSharedSurface 函式

抓取支援指定視窗的 DirectX 共用介面。 您可以將這個介面寫入，以便更新視窗的內容。

## <a name="syntax"></a>語法

```C++
HRESULT WINAPI DwmDxGetWindowSharedSurface(
  _In_     HWND        hwnd,
  _In_     LUID        luidAdapter,
  _In_opt_ HMONITOR    hmonitorAssociation,
  _In_     DWORD       dwFlags,
  _Inout_  DXGI_FORMAT *pfmtWindow,
  _Out_    HANDLE      *phDxSurface,
  _Out_    UINT64      *puiUpdateId
);
```

## <a name="parameters"></a>參數

`hwnd`

指定要更新之視窗的 [**HWND**](/windows/desktop/winprog/windows-data-types) 。

`luidAdapter`

介面所在的介面卡的 [**LUID**](/previous-versions/bb401655(v%3dmsdn.10)) 。

`hmonitorAssociation`

保留的。

`dwFlags`

這個參數可以是下列其中一個值，或是在適當的情況下，多個值的位 OR 組合。

| 值 | 意義 |
|-|-|
| <span id="DWM_REDIRECTION_FLAG_WAIT"></span><span id="dwm_redirection_flag_wait"></span><dl> <dt>**DWM \_重新導向 \_ 旗標 \_ 等候**</dt> <dt>0</dt> </dl> | 導致函式封鎖，直到上次呼叫函式之後， (VSync) 已過為止。 |
| <span id="DWM_REDIRECTION_FLAG_SUPPORT_PRESENT_TO_GDI_SURFACE"></span><span id="dwm_redirection_flag_support_present_to_gdi_surface"></span><dl> <dt>**DWM \_\_ \_ \_ 存在 \_ 于 \_ GDI \_ 介面**</dt> <dt>0x10</dt>的重新導向旗標支援 </dl> | 指出呼叫的應用程式能夠向 GDI 共用介面呈現。 |

`pfmtWindow`

輸入時所需的介面格式。 在輸出時，傳回介面的實際格式。

`phDxSurface`

在輸出時，為介面的共用控制碼。

`puiUpdateId`

在輸出時，更新的識別碼。

## <a name="return-value"></a>傳回值

此函數可以傳回其中一個值。

| 傳回碼 | Description |
|-|-|
| **S \_ 確定** | 呼叫成功，您應該更新介面，在提交更新時，請務必將更新識別碼傳遞至 D3DKMT 轉譯結構的 **PresentHistoryToken** 成員中 **的 \_** [D3DKMTRender](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtrender) (，然後使用相同的更新識別碼來呼叫 [**DwmDxUpdateWindowSharedSurface**](dwmdxupdatewindowsharedsurface.md) 。 請注意，不論是否已實際更新介面，都應該呼叫 **DwmDxUpdateWindowSharedSurface** 。 |
| **DWM \_ S \_ GDI 重新導向 \_ \_ 介面** | 呼叫成功，您應該呼叫 [D3DKMTPresent](/windows-hardware/drivers/ddi/content/d3dkmthk/nf-d3dkmthk-d3dkmtpresent)來更新介面，並將 **PresentHistoryToken** 成員的 **模型** 設定為 **D3DKMT PM 重新 \_ \_ 導向 \_ BLT**，並在聯集的 **BLT** 成員中提供更新識別碼。 只有在 *dwFlags* 中指定了 **針對 \_ \_ \_ \_ \_ \_ GDI \_ 介面提供的 DWM** 重新導向旗標支援時，才會傳回這個值。 |
| **\_ \_ \_ \_ 找不到 DWM E ADAPTER** | *LuidAdapter* 的值無效。 |
| **DWM \_ E \_ COMPOSITIONDISABLED** | DWM 目前未啟用，且應用程式必須以另一種方式呈現。 |

## <a name="remarks"></a>備註

此 API 適用于執行圖形驅動程式或執行時間。 應用程式可能不會呼叫這個方法。 本檔僅適用于 Windows 7，而且此 API 不保證存在，也不會在其他 Windows 版本上以類似的方式運作。 此函式不會出現在任何標頭或靜態程式庫中，而且位於 dwmapi.dll 的序數100。

## <a name="requirements"></a>規格需求

| 需求 | 值 |
|-|-|
| 最低支援的用戶端 | \[僅限 Windows 7 桌面應用程式\] |
| 最低支援的伺服器 | 都不支援 |
| 用戶端支援結束 | Windows 7 |
| 標頭 | N/A |
| DLL | Dwmapi.dll |
