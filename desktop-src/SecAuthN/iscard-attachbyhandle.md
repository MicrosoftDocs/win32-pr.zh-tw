---
description: 將 ISCard 物件附加至開啟和設定的智慧卡控點。
ms.assetid: e735d33d-a337-404e-a760-4cf8f19d172a
title: 'ISCard：： AttachByHandle 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.AttachByHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: e72ce215b373ef8bd48921f796083e9bc5e801be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106990409"
---
# <a name="iscardattachbyhandle-method"></a>ISCard：： AttachByHandle 方法

\[**AttachByHandle** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**AttachByHandle** 方法會將 [**ISCard**](iscard.md)物件附加至開啟和設定的 [*智慧卡*](../secgloss/s-gly.md)控制碼。

## <a name="syntax"></a>語法


```C++
HRESULT AttachByHandle(
  [in] HSCARD hCard
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*hCard* \[在\]
</dt> <dd>

智慧卡的開啟連接控制碼。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                    |
|----------------------------------------------------------------------------------------------|------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>   |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *HCard* 參數無效。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

當您完成使用控制碼時，請呼叫 [**ISCard：:D etach**](iscard-detach.md) 方法來釋放附件。

## <a name="examples"></a>範例

下列範例顯示如何附加至智慧卡控制碼。


```C++
HRESULT  hr;

// hSC is of type HSCARD and has been previously assigned.
// Attach SCard to the smart card using the value in hSC.
hr = pISCard->AttachByHandle(hSC);
if (FAILED(hr))
{
   printf("Failed AttachByHandle\n");
   // Take other error handling action as needed.
}
// Proceed using attached reader.
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

[**AttachByReader**](iscard-attachbyreader.md)
</dt> <dt>

[**中斷連結**](iscard-detach.md)
</dt> <dt>

[**取得 \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> <dt>

[**附加**](iscard-reattach.md)
</dt> </dl>

 

 
