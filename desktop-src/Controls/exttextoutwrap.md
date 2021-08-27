---
title: ExtTextOutWrap 函式
description: 使用目前選取的字型、背景色彩和文字色彩來繪製文字。 您可以選擇性地提供要用於剪切、不透明度或兩者的維度。 此函數會包裝對 ExtTextOut 的呼叫。
ms.assetid: 0804c231-53f9-4de6-b703-0077cdcebcb5
keywords:
- ExtTextOutWrap 函式 Windows 控制項
topic_type:
- apiref
api_name:
- ExtTextOutWrap
api_location:
- Comctl32.dll
api_type:
- DllExport
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 934a8d203cf232a339db46e97783e87c075e5bb949ec5d23e20a7b1874ea6ef2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120047268"
---
# <a name="exttextoutwrap-function"></a>ExtTextOutWrap 函式

\[**ExtTextOutWrap** 可透過 Windows XP Service Pack 2 (SP2) 取得。 它可能會在後續版本中變更或無法使用。 建議您改為直接使用 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 。\]

使用目前選取的字型、背景色彩和文字色彩來繪製文字。 您可以選擇性地提供要用於剪切、不透明度或兩者的維度。 此函數會包裝對 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)的呼叫。

## <a name="syntax"></a>語法


```C++
BOOL ExtTextOutWrap(
  _In_       HDC     hdc,
  _In_       int     X,
  _In_       int     Y,
  _In_       UINT    uOptions,
  _In_ const RECT    *lprc,
  _In_       LPCTSTR lpString,
  _In_       UINT    cbCount,
  _In_ const INT     *lpDx
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hdc* \[在\]
</dt> <dd>

類型： **[ **HDC**](/windows/desktop/WinProg/windows-data-types)**

裝置內容的控制碼。

</dd> <dt>

*X* \[ 于\]
</dt> <dd>

類型： **int**

用來定位字串之參考點的 x 座標（以邏輯座標表示）。

</dd> <dt>

*Y* \[ in\]
</dt> <dd>

類型： **int**

用來放置字串的參考點的 y 座標（以邏輯座標表示）。

</dd> <dt>

*uOptions* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

值，指定如何使用應用程式定義的矩形。 如需完整的選項清單，請參閱 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 。

</dd> <dt>

*lprc* \[在\]
</dt> <dd>

Type： **Const [**RECT**](/previous-versions//dd162897(v=vs.85)) \***

選擇性 [**RECT**](/previous-versions//dd162897(v=vs.85)) 結構的指標，此結構會指定用於裁剪、不透明度或兩者之矩形的維度（以邏輯座標表示）。

</dd> <dt>

*lpString* \[在\]
</dt> <dd>

類型： **[ **LPCTSTR**](/windows/desktop/WinProg/windows-data-types)**

包含要繪製之文字的緩衝區指標。 字串不需要以零結束，因為 *cbCount* 會指定字串的長度。

</dd> <dt>

*cbCount* \[在\]
</dt> <dd>

類型： **[ **UINT**](/windows/desktop/WinProg/windows-data-types)**

*LpString* 所指向的字串長度（以位元組為單位）。

</dd> <dt>

*lpDx* \[在\]
</dt> <dd>

類型： **Const [**INT**](/windows/desktop/WinProg/windows-data-types) \***

值的選擇性陣列指標，表示相鄰字元資料格來源之間的距離。 例如， *lpDx* \[ x \] 邏輯單元分隔字元資料格 x 和字元資料格的來源 (x + 1) 。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **[ **BOOL**](/windows/desktop/WinProg/windows-data-types)**

如果成功繪製字串，則傳回非零值。 但是，如果 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta) 的 ANSI 版本是以 ETO 圖像索引來呼叫 \_ ，則函式會傳回 \_ **TRUE** ，即使函數沒有任何作用也一樣。

如果此函式失敗，則傳回值為零。

若要取得擴充的錯誤資訊，請呼叫 [**GetLastError**](/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror)。

## <a name="remarks"></a>備註

**ExtTextOutWrap** 不會依名稱匯出，也不會在公用標頭檔中宣告。 若要使用它，您必須從 ComCtl32.dll 使用 [**GetProcAddress**](/windows/desktop/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數417來取得函式指標。

如需其他備註，請參閱 [**ExtTextOut**](/windows/desktop/api/wingdi/nf-wingdi-exttextouta)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                                                 |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Comctl32.dll (6.0 版或更新版本) </dt> </dl> |



 

