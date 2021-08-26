---
description: 使用智慧卡資源管理員所傳回的控制碼，建立智慧卡 (ICC) 的通訊連結。
ms.assetid: dfd05dce-4416-4881-92ca-c85baccf3b86
title: ISCardManage：： AttachByHandle 方法
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardManage.AttachByHandle
api_type:
- COM
api_location: ''
ms.openlocfilehash: c464f2d514a59754b5dc4d9d98f745a4802843c3cfafa3df16057c53456221c5
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120014158"
---
# <a name="iscardmanageattachbyhandle-method"></a>ISCardManage：： AttachByHandle 方法

\[**AttachByHandle** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**AttachByHandle** 方法會使用智慧卡 [*資源管理員*](../secgloss/r-gly.md)所傳回的控制碼，建立 [*智慧卡*](../secgloss/s-gly.md) (ICC) 的通訊連結。

## <a name="syntax"></a>語法


```C++
HRESULT AttachByHandle(
  [in] HSCARD hICC
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hICC* \[在\]
</dt> <dd>

智慧卡的控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值：



| 傳回碼                                                                                   | 描述                                   |
|-----------------------------------------------------------------------------------------------|-----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>          | 作業順利完成。<br/>  |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl>  | *HICC* 參數無效。<br/> |
| <dl> <dt>**E \_ OUTOFMEMORY**</dt> </dl> | 記憶體不足。<br/>                     |



 

## <a name="remarks"></a>備註

附加 [*讀取器*](../secgloss/r-gly.md) 呼叫 [**AttachByIFD**](iscardmanage-attachbyifd.md)。

若要釋放附件呼叫卸 [**離**](iscardmanage-detach.md)。

若要在不呼叫卸 [**離**](iscardmanage-detach.md) 和 **AttachByHandle** 的情況下與智慧卡重新連接，請呼叫 [**reconnect**](iscardmanage-reconnect.md)。

如需 [**ISCardManage**](iscardmanage.md) 介面所定義之所有方法的清單，請參閱 [**ISCardManage**](iscardmanage.md)。

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需智慧卡錯誤碼的詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>          |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/> |
| 用戶端支援結束<br/>    | Windows XP<br/>                                |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                       |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AttachByIFD**](iscardmanage-attachbyifd.md)
</dt> <dt>

[**中斷連結**](iscardmanage-detach.md)
</dt> <dt>

[**ISCardManage**](iscardmanage.md)
</dt> <dt>

[**重新連接**](iscardmanage-reconnect.md)
</dt> </dl>

 

 
