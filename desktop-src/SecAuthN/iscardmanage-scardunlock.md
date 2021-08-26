---
description: 釋出已連接智慧卡的專用用途。
ms.assetid: a236743a-1d12-44db-853d-f757f43a7e8f
title: ISCardManage：： SCardUnlock 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.SCardUnlock
api_type:
- COM
api_location: ''
ms.openlocfilehash: 1c100d1607cceea95264e9af24ba29b23824dee833c14e492cfb0a1dd7ad396f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013888"
---
# <a name="iscardmanagescardunlock-method"></a>ISCardManage：： SCardUnlock 方法

\[**SCardUnlock** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**SCardUnlock** 方法會釋出已連接 [*智慧卡*](../secgloss/s-gly.md)的專用用途。

## <a name="syntax"></a>語法


```C++
HRESULT SCardUnlock(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*處置* \[在\]
</dt> <dd>

釋放鎖定時要離開智慧卡的狀態。

<dl><span id="LEAVE"></span><span id="leave"></span><dt>

**離開**
</dt><span id="RESET"></span><span id="reset"></span><dt>

**RESET**
</dt><span id="UNPOWER"></span><span id="unpower"></span><dt>

**UNPOWER**
</dt><span id="EJECT"></span><span id="eject"></span><dt>

**彈出**
</dt> </dl> </dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | 描述                                          |
|----------------------------------------------------------------------------------------------|------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>         |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *處置* 參數無效。<br/> |



 

## <a name="remarks"></a>備註

若要鎖定連接的智慧卡，請呼叫 [**SCardLock**](iscardmanage-scardlock.md)。

如需此介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

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
</dt> <dt>

[**SCardLock**](iscardmanage-scardlock.md)
</dt> </dl>

 

 
