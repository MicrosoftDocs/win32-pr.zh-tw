---
title: DrawTextWrap 函式
description: 在指定的矩形中繪製格式化的文字。 它會根據指定的方法將文字格式化 (展開索引標籤、對齊字元、斷線等) 。 此函數會包裝對 DrawText 的呼叫。
ms.assetid: 28ab4c5e-3b8f-49e8-b072-500ba1916caf
keywords:
- DrawTextWrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- DrawTextWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: cfc5eb707b4016a592ad339223e0f32ab21d4a29
ms.sourcegitcommit: a1494c819bc5200050696e66057f1020f5b142cb
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/12/2020
ms.locfileid: "103933967"
---
# <a name="drawtextwrap-function"></a>DrawTextWrap 函式

\[**DrawTextWrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能會在後續版本中變更或無法使用。 建議您改為直接使用 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 。\]

在指定的矩形中繪製格式化的文字。 它會根據指定的方法將文字格式化 (展開索引標籤、對齊字元、斷線等) 。 此函數會包裝對 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)的呼叫。

## <a name="syntax"></a>語法


```C++
int WINAPI DrawTextWrap(
  _In_    HDC              hdc,
  _Inout_ LPCTSTR          lpString,
  _In_    int              nCount,
  _Inout_ LPRECT           lpRect,
  _In_    UINT             uFormat,
  _In_    LPDRAWTEXTPARAMS lpDTParams
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* \[在\]
</dt> <dd>

類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

裝置內容的控制碼。

</dd> <dt>

*lpString* \[in、out\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

包含要繪製之文字的緩衝區指標。 如果 *nCount* 參數為-1，則字串必須以 null 結束。

如果 *uFormat* 包含 DT \_ MODIFYSTRING，此函式最多可能會在此字串中加上四個額外的字元。 包含字串的緩衝區必須夠大，才能容納這些額外的字元。

</dd> <dt>

*nCount* \[在\]
</dt> <dd>

類型： **int**

*LpString* 所指向之字串的長度。 如果 *nCount* 為-1，則會假設 *lpString* 參數是以 null 終止之字串的指標，而 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 會自動計算字元計數。

</dd> <dt>

*lpRect* \[in、out\]
</dt> <dd>

類型： **LPRECT**

[**矩形結構的**](/previous-versions//dd162897(v=vs.85))指標，其中包含要格式化文字的矩形（以邏輯座標表示）。

</dd> <dt>

*uFormat* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

格式化選項。 如需完整的選項清單，請參閱 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext) 檔。

</dd> <dt>

*lpDTParams* \[在\]
</dt> <dd>

類型： **LPDRAWTEXTPARAMS**

[**DRAWTEXTPARAMS**](/windows/win32/api/winuser/ns-winuser-drawtextparams)結構的指標，指定其他格式化選項。 此參數可以是 **Null**。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **int**

如果函式成功，則傳回值為邏輯單元中的文字高度。 如果指定了 **DT \_ VCENTER** 或 **Dt \_ 底端**，則如果函式失敗，則傳回值是 *lprc* **頂端** 成員到所繪製文字底部的位移，而傳回值為零。

如果此函式失敗，則傳回值為零。

若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**DrawTextWrap** 不會依名稱匯出，也不會在公用標頭中宣告。 若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數415來取得函式指標。

如需其他備註，請參閱 [**DrawText**](/windows/desktop/api/winuser/nf-winuser-drawtext)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 Windows Vista 桌面應用程式\]<br/>                                                                 |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (6.0 版或更新版本) </dt> </dl> |



 

