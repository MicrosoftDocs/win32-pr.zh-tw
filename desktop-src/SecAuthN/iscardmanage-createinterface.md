---
description: 建立指定的介面。
ms.assetid: f4cfc407-b006-46a2-9751-834b532309ec
title: ISCardManage：： CreateInterface 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.CreateInterface
api_type:
- COM
api_location: ''
ms.openlocfilehash: 8c9b231ec7930b78c1693e38268638e7a24b26dfa32d8f25acb5a429dbcdedc1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118922657"
---
# <a name="iscardmanagecreateinterface-method"></a>ISCardManage：： CreateInterface 方法

\[**CreateInterface** 方法可用於 [需求] 區段中指定的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**CreateInterface** 方法會建立指定的介面。

## <a name="syntax"></a>語法


```C++
HRESULT CreateInterface(
  [in]  LPGUID    pguidInterface,
  [in]  BSTR      bstrName,
  [in]  LONG      *pUserData,
  [out] LPUNKNOWN *ppInterface
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pguidInterface* \[在\]
</dt> <dd>

要建立之介面的 GUID 值。

</dd> <dt>

*bstrName* \[在\]
</dt> <dd>

GUID 無法使用時所要建立的介面名稱。 標準值為 "CryptoProvider"。

</dd> <dt>

*pUserData* \[在\]
</dt> <dd>

要在建立介面時使用之使用者特定資料的指標。

</dd> <dt>

*ppInterface* \[擴展\]
</dt> <dd>

傳回之介面的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

可能的傳回值如下：



| 傳回碼                                                                                   | 描述                                                                                      |
|-----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | 其中一個提供的參數無效。<br/>                                         |
| <dl> <dt>**E \_ 指標**</dt> </dl>     | 在 *pguidInterface* 或 *pUserData* 參數中傳遞了錯誤指標。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                                                                        |



 

## <a name="remarks"></a>備註

如需 [**ISCardManage**](iscardmanage.md) 介面所定義之所有方法的清單，請參閱 **ISCardManage**。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回 [*智慧卡*](../secgloss/s-gly.md) 的錯誤碼。 如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

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

 

 
