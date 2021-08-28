---
description: 建立 ISCardAuth 介面。
ms.assetid: a091e361-416e-45c9-8077-617b16db654c
title: ISCardManage：： CreateCardAuth 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateCardAuth
api_type:
- COM
api_location: ''
ms.openlocfilehash: f6f78e938e8c739bcc2bca6c2ce7769d64d6f72ad02296aa9b2fb692d6c129a0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014128"
---
# <a name="iscardmanagecreatecardauth-method"></a>ISCardManage：： CreateCardAuth 方法

\[**CreateCardAuth** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**CreateCardAuth** 方法會建立 [**ISCardAuth**](iscardauth.md)介面。

## <a name="syntax"></a>語法


```C++
HRESULT CreateCardAuth(
  [out] ISCardAuth **ppISCardAuth
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ppISCardAuth* \[擴展\]
</dt> <dd>

傳回已建立介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | 描述                                            |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>           |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *PpISCardAuth* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *ppISCardAuth* 中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                              |



 

## <a name="remarks"></a>備註

如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
