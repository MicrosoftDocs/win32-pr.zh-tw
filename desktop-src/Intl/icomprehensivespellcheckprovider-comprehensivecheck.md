---
description: 以更完整的方式檢查提供者文字，而不是 ISpellCheckProvider：： Check。
ms.assetid: BD334EB8-4E14-478D-AB2A-E7F863C4BE0F
title: IComprehensiveSpellCheckProvider：： ComprehensiveCheck 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IComprehensiveSpellCheckProvider.ComprehensiveCheck
api_type:
- COM
api_location:
- spellcheckprovider.h
ms.openlocfilehash: d999a90166e0d54d537abc84c30f6c4e0ee3768c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106977105"
---
# <a name="icomprehensivespellcheckprovidercomprehensivecheck-method"></a>IComprehensiveSpellCheckProvider：： ComprehensiveCheck 方法

以更完整的方式檢查提供者文字，而不是 [**ISpellCheckProvider：： check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)。

## <a name="syntax"></a>語法


```C++
HRESULT ComprehensiveCheck(
  [in]  PCWSTR             text,
  [out] IEnumSpellingError **result
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*文字* \[在\]
</dt> <dd>

要檢查的文字。

</dd> <dt>

*結果* \[擴展\]
</dt> <dd>

檢查此文字的結果，如拼寫錯誤的列舉 ([**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)) （如果有的話）。

</dd> </dl>

## <a name="return-value"></a>傳回值

這個方法可以傳回其中一個值。



| 傳回值                                                                             | 描述                           |
|------------------------------------------------------------------------------------------|---------------------------------------|
| <dl> <dt>S \_ 確定</dt> </dl>         | 成功。<br/>                |
| <dl> <dt>E \_ INVALIDARG</dt> </dl> | *文字* 是空字串。<br/> |
| <dl> <dt>E \_ 指標</dt> </dl>    | *文字* 是 null 指標。<br/>  |



 

## <a name="remarks"></a>備註

這個介面不需要由拼寫檢查提供者來執行。 但是，如果提供者支援兩種拼寫檢查的「模式」 (更快速且更慢但更徹底的) ，則應該在執行 [**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider) 的相同物件中執行這個介面，以支援更徹底的檢查模式。 當用戶端呼叫 [**ISpellChecker：： ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)時，拼寫檢查功能將會對 [**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)的提供者進行 [**QueryInterface**](/windows/win32/api/unknwn/nf-unknwn-iunknown-queryinterface(q))程式，並在支援介面時呼叫 **IComprehensiveSpellCheckProvider. ComprehensiveCheck** 。 如果介面不受支援，則會以無訊息模式切換回 [**ISpellCheckProvider：： Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)。

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**IComprehensiveSpellCheckProvider**](/windows/desktop/api/spellcheckprovider/nn-spellcheckprovider-icomprehensivespellcheckprovider)
</dt> <dt>

[**IEnumSpellingError**](/windows/desktop/api/Spellcheck/nn-spellcheck-ienumspellingerror)
</dt> <dt>

[**ISpellChecker::ComprehensiveCheck**](/windows/desktop/api/Spellcheck/nf-spellcheck-ispellchecker-comprehensivecheck)
</dt> <dt>

[**ISpellCheckProvider**](/windows/desktop/api/Spellcheckprovider/nn-spellcheckprovider-ispellcheckprovider)
</dt> <dt>

[**ISpellCheckProvider：： Check**](/windows/desktop/api/Spellcheckprovider/nf-spellcheckprovider-ispellcheckprovider-check)
</dt> </dl>

 

 
