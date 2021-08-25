---
description: 分別釋出 AttachByHandle 和 AttachByIFD 所配置的特定智慧卡或讀取器的附件。
ms.assetid: 601b35a6-9094-4786-b94c-5cd1283feef5
title: ISCardManage：:D etach 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.Detach
api_type:
- COM
api_location: ''
ms.openlocfilehash: 067c8e9f3e8cee607281d5f0a80ca813e91b425e63c15d3c1d47661acbbd04d9
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014088"
---
# <a name="iscardmanagedetach-method"></a>ISCardManage：:D etach 方法

\[卸 **離** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

卸 **離** 方法會分別將附件釋出至特定 [*智慧卡*](../secgloss/s-gly.md)或 [**AttachByHandle**](iscardmanage-attachbyhandle.md)和 [**AttachByIFD**](iscardmanage-attachbyifd.md)所配置的 [*讀取器*](../secgloss/r-gly.md)。

## <a name="syntax"></a>語法


```C++
HRESULT Detach();
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

若要在不呼叫卸 **離** 和 [**AttachByHandle**](iscardmanage-attachbyhandle.md)的情況下與智慧卡重新連接，請呼叫 [**reconnect**](iscardmanage-reconnect.md)。

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

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**重新連接**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
