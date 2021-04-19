---
description: 關閉智慧卡的開啟連接。
ms.assetid: 7d768945-8d5d-4d29-b5bc-1b2ac5b0e114
title: 'ISCard：:D etach 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.Detach
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: f9fd2b2a6d9ea2df8e886c6ff9851706c2030a1d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "107001423"
---
# <a name="iscarddetach-method"></a>ISCard：:D etach 方法

\[卸 **離** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

卸 **離** 方法會關閉 [*智慧卡*](../secgloss/s-gly.md)的開啟連接。

## <a name="syntax"></a>語法


```C++
HRESULT Detach(
  [in] SCARD_DISPOSITIONS Disposition
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*處置* \[在\]
</dt> <dd>

指出在連接的 [*讀取器*](../secgloss/r-gly.md)中應如何使用卡片進行哪些操作。



| 值                                                                                                                                      | 意義                                                                                                            |
|--------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------------|
| <span id="LEAVE"></span><span id="leave"></span><dl> <dt>**離開**</dt> </dl>       | 將智慧卡保留為目前的 [*狀態*](../secgloss/s-gly.md)。<br/> |
| <span id="RESET"></span><span id="reset"></span><dl> <dt>**重 置**</dt> </dl>       | 將智慧卡重設為某個已知狀態。<br/>                                                              |
| <span id="UNPOWER"></span><span id="unpower"></span><dl> <dt>**UNPOWER**</dt> </dl> | 移除智慧卡的電源。<br/>                                                                      |
| <span id="EJECT"></span><span id="eject"></span><dl> <dt>**彈出**</dt> </dl>       | 如果讀取器有退出功能，請將智慧卡彈出。<br/>                                             |



 

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                  |
|----------------------------------------------------------------------------------------------|----------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | 配置 *無效。*<br/>       |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示關閉智慧卡的連接。


```C++
HRESULT    hr;

// Detach the smart card.
hr = pISCard->Detach(LEAVE);
if (FAILED(hr))
{
   printf("Failed Detach\n");
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

[**ISCard**](iscard.md)
</dt> <dt>

[**附加**](iscard-reattach.md)
</dt> </dl>

 

 
