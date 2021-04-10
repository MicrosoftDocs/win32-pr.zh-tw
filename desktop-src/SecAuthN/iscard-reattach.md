---
description: 重新附加方法會重設或重新初始化智慧卡。
ms.assetid: c9cd9cd7-5ee6-48dc-8460-deb9c827fcc4
title: 'ISCard：：重新附加方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.ReAttach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 3f5ff4cd46b2b523b0031e1389b96d9c2c3973a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191855"
---
# <a name="iscardreattach-method"></a>ISCard：：重新附加方法

\[[重新 **附加** ] 方法可在 [需求] 區段中指定的作業系統中使用。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

重新 **附加** 方法會重設或重新初始化 [*智慧卡*](../secgloss/s-gly.md)。

## <a name="syntax"></a>語法


```C++
HRESULT ReAttach(
  [in] SCARD_SHARE_MODES  ShareMode,
  [in] SCARD_DISPOSITIONS InitState
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*ShareMode* \[在\]
</dt> <dd>

要在其中共用或獨佔擁有智慧卡連接的模式。



| 值                                                                                                                                            | 意義                                                       |
|--------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------|
| <span id="EXCLUSIVE"></span><span id="exclusive"></span><dl> <dt>**獨家**</dt> </dl> | 沒有其他人使用此智慧卡連線。<br/> |
| <span id="SHARED"></span><span id="shared"></span><dl> <dt>**共用**</dt> </dl>          | 其他應用程式可以使用此連接。<br/>        |



 

</dd> <dt>

*InitState* \[在\]
</dt> <dd>

指出如何處理卡片。



| 值                                                                                                                                      | 意義                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**離開**</dt> </dl>       | 將智慧卡保留為目前的 [*狀態*](../secgloss/s-gly.md)。<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**重 置**</dt> </dl>       | 將智慧卡重設為某個已知狀態。<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | 移除智慧卡的電源。<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**彈出**</dt> </dl>       | 如果讀取器有退出功能，請將智慧卡彈出。<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                                                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>                                                     |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 傳遞至函式的一或多個參數發生問題。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示重新初始化智慧卡。


```C++
HRESULT    hr;

// Reattach the smart card.
hr = pISCard->ReAttach(SHARED, LEAVE);
if (FAILED(hr))
{
   printf("Failed ReAttach\n");
   // Take error handling action as needed.
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | \[僅限 WINDOWS XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | 僅限 Windows Server 2003 \[ desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scardmgr。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scardmgr .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCard 定義為1461AAC3-6810-11D0-918F-00AA00C18068<br/>               |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**AttachByHandle**](iscard-attachbyhandle.md)
</dt> <dt>

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**中斷連結**](iscard-detach.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
