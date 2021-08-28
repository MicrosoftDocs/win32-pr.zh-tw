---
description: 判斷是否已在作業系統上安裝或支援依名稱指定的地區設定。
ms.assetid: 6df92e4d-d78e-48b5-9515-18f0497de95b
title: 'RtlIsValidLocaleName 函式 (Ntrtl) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- RtlIsValidLocaleName
api_type:
- DllExport
api_location:
- Kernel32.dll
ms.openlocfilehash: 993d819324987fccdfb66c26343bccfb9a815606655a18ff1a1e43f9a2af0eac
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130278"
---
# <a name="rtlisvalidlocalename-function"></a>RtlIsValidLocaleName 函式

判斷是否已在作業系統上安裝或支援依名稱指定的地區設定。

> [!Note]  
> 這項功能僅適用于 Windows Vista。 它可能會在後續版本中變更或無法使用。 應用程式應該使用 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)。

 

## <a name="syntax"></a>語法


```C++
BOOL RtlIsValidLocaleName(
  _In_ LPCWSTR LocaleName,
  _In_ ULONG   Flags
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*>Localename* \[在\]
</dt> <dd>

要驗證的[地區設定名稱](locale-names.md)。 此參數可指定 [自訂地區](custom-locales.md)設定的名稱。

</dd> <dt>

*旗標* \[在\]
</dt> <dd>

指出中性地區設定是否視為有效的旗標。 目前唯一定義的旗標是 [地區設定 \_ 允許 \_ 中立](locale-allow-neutral.md)的。 預設值為不是。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果成功，則傳回非零值，否則傳回0。

## <a name="remarks"></a>備註

此函數類似于 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)。 唯一的差別在於，如果 \_ \_ 設定了 LOCALE 允許中性， **RtlIsValidLocaleName** 會針對對應至中性 (地區設定的名稱傳回 **true** ，例如 "en" ) ，而 [**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename) 只會針對特定 (地區設定傳回 **true** ，例如 "en-us" ) 。 Windows Vista （含）以後版本的資源載入策略會使用中性地區設定。 只有小型的高度特製化應用程式會使用 **RtlIsValidLocaleName** 並設定地區設定 \_ \_ ，因為中性地區設定的用途有限。 [呼叫「地區設定名稱](calling-the--locale-name--functions.md)」函式中所述的任何函式都不接受中性地區設定做為輸入。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 Vista desktop 應用程式\]<br/>                                          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2008 desktop 應用程式\]<br/>                                    |
| 標頭<br/>                   | <dl> <dt>Ntrtl。h</dt> </dl>      |
| 程式庫<br/>                  | <dl> <dt>Kernel32.lib</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Kernel32.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[國家語言支援](national-language-support.md)
</dt> <dt>

[國家語言支援功能](national-language-support-functions.md)
</dt> <dt>

[**IsValidLocaleName**](/windows/desktop/api/Winnls/nf-winnls-isvalidlocalename)
</dt> </dl>

 

 




