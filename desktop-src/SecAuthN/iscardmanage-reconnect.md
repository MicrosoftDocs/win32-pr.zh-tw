---
description: 允許應用程式重新連線到智慧卡或讀取器，而不需要分別發出卸離呼叫和 AttachByHandle 或 AttachByIFD 呼叫。
ms.assetid: 450e817d-2cb2-4752-a86e-50cc8e434723
title: ISCardManage：： Reconnect 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Reconnect
api_type:
- COM
api_location: ''
ms.openlocfilehash: 9c0359a062f62e49b52b92623714e6d94aff015e53a71afa45d4a433c31f28c0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120013978"
---
# <a name="iscardmanagereconnect-method"></a>ISCardManage：： Reconnect 方法

\[**Reconnect** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Reconnect** 方法可讓應用程式重新連線到 [*智慧卡*](../secgloss/s-gly.md)或 [*讀取器*](../secgloss/r-gly.md)，而不需要分別發出卸 [**離**](iscardmanage-detach.md)呼叫，然後再發出 [**AttachByHandle**](iscardmanage-attachbyhandle.md)或 [**AttachByIFD**](iscardmanage-attachbyifd.md)呼叫。

## <a name="syntax"></a>語法


```C++
HRESULT Reconnect();
```



## <a name="parameters"></a>參數

這個方法沒有任何參數。

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | 描述                                  |
|-----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                    |



 

## <a name="remarks"></a>備註

連接智慧卡呼叫 [**AttachByHandle**](iscardmanage-attachbyhandle.md) 或 [**AttachByIFD**](iscardmanage-attachbyifd.md)。

若要卸離智慧卡，請呼叫卸 [**離**](iscardmanage-detach.md)。

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

[**AttachByHandle**](iscardmanage-attachbyhandle.md)
</dt> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**中斷連結**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> </dl>

 

 
