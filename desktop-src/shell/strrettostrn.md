---
description: 採用 IShellFolder：： GetDisplayNameOf 傳回的 STRRET 結構，將它轉換成字串，並將結果放在緩衝區中。
title: StrRetToStrN 函式
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- StrRetToStrN
api_type:
- DllExport
api_location:
- Shell32.dll
ms.assetid: a816fb5f-8320-4b63-a85d-dd4c59596ead
ms.openlocfilehash: 89a8d991e22e8615456bd8d4690c046ec0d325d3
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104991810"
---
# <a name="strrettostrn-function"></a>StrRetToStrN 函式

採用 [**IShellFolder：： GetDisplayNameOf**](/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getdisplaynameof)傳回的 [**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret)結構，將它轉換成字串，並將結果放在緩衝區中。

## <a name="syntax"></a>語法


```C++
BOOL StrRetToStrN(
  _Out_   LPTSTR        pszOut,
  _In_    UINT          cchOut,
  _Inout_ LPSTRRET      pStrRet,
  _In_    LPCITEMIDLIST pidl
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pszOut* \[擴展\]
</dt> <dd>

類型： **LPTSTR**

保存顯示名稱的緩衝區。 它會以 null 終止字串的形式傳回。 如果 *cchOut* 太小，名稱將會被截斷以配合其大小。

</dd> <dt>

*cchOut* \[在\]
</dt> <dd>

類型： **UINT**

*PszOut* 的大小（以字元為單位）。 如果 *cchOut* 太小，則字串將會被截斷以配合其大小。

</dd> <dt>

*pStrRet* \[in、out\]
</dt> <dd>

類型： **LPSTRRET**

[**STRRET**](/windows/desktop/api/Shtypes/ns-shtypes-strret)結構的指標。 當函式傳回時，這個指標將不再有效。

</dd> <dt>

*pidl* \[在\]
</dt> <dd>

類型： **LPCITEMIDLIST**

專案之 [**ITEMIDLIST**](/windows/desktop/api/Shtypes/ns-shtypes-itemidlist) 結構的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

類型： **BOOL**

若為成功，**則為 TRUE** ，如果失敗，則為 **FALSE** 。

## <a name="remarks"></a>備註

> [!Note]  
> 從 Shell32.dll 5.0 版起，呼叫此函式相當於呼叫 [**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)。

 

**StrRetToStrN** 不是依名稱匯出。 若要使用它，您必須從 Shell32.dll 使用 [**GetProcAddress**](/windows/win32/api/libloaderapi/nf-libloaderapi-getprocaddress) 和要求序數96來取得函式指標。

如果 *pStrRet* 所指向之結構的 **uType** 成員設定為 **STRRET \_ WSTR**，該結構的 **pOleStr** 成員將會在傳回時釋出。

請注意，此函式會從 Shell32.dll 匯出，而不是 Shlwapi.dll。 它也包含在 Shlobj.h 中，而不是 Shlwapi。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | 僅限 windows 2000 Professional、Windows XP \[ desktop 應用程式\]<br/>                                         |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                           |
| DLL<br/>                      | <dl> <dt>Shell32.dll (4.71 版或更新版本) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**StrRetToStr**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettostra)
</dt> <dt>

[**StrRetToBuf**](/windows/desktop/api/Shlwapi/nf-shlwapi-strrettobufa)
</dt> </dl>

 

 
