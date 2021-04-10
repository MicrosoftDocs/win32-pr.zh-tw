---
description: 抓取已連接智慧卡的控制碼。 \*如果未連接，這個方法會傳回 (pHandle) = = Null。
ms.assetid: f03f8f25-b2e4-4fae-b7d2-bb0f1a7cd987
title: 'ISCard：： get_CardHandle 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_CardHandle
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: d7e945f0f4a300dfed444c7e8f5921b806d96b1c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103936611"
---
# <a name="iscardget_cardhandle-method"></a>ISCard：： get \_ CardHandle 方法

\[**Get \_ CardHandle** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ CardHandle** 方法會抓取連接 [*智慧卡*](../secgloss/s-gly.md)的控制碼。 \*如果未連接，這個方法會傳回 (pHandle) = = **Null** 。

## <a name="syntax"></a>語法


```C++
HRESULT get_CardHandle(
  [out] HSCARD *pHandle
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pHandle* \[擴展\]
</dt> <dd>

傳回時的智慧卡控制碼指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                       |
|----------------------------------------------------------------------------------------------|---------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>      |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PHandle* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 在 *pHandle* 中傳遞了錯誤指標。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示如何取出智慧卡控制碼。


```C++
HSCARD   hSC;
HRESULT  hr;

// Retrieve the card handle.
hr = pISCard->get_CardHandle(&hSC);
if (FAILED(hr))
{
   printf("Failed get_CardHandle\n");
   // Take other error handling action as needed.
}
// Use card handle as needed.
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

[**取得 \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**取得 \_ 內容**](iscard-get-context.md)
</dt> <dt>

[**取得 \_ 通訊協定**](iscard-get-protocol.md)
</dt> <dt>

[**取得 \_ 狀態**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
