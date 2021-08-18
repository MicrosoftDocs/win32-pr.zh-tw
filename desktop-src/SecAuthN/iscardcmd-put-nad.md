---
description: 指定要搭配 ISCardCmd 介面使用 (Nad) 的節點位址。
ms.assetid: 49de8264-9491-41a4-a8e0-68d0db088ded
title: 'ISCardCmd：:p ut_Nad 方法 (Scarddat .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCardCmd.put_Nad
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: 84ade2e2ca69c328650f4c7df485814e4eaacedf3fdb0190fc883cde864a8082
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119481388"
---
# <a name="iscardcmdput_nad-method"></a>ISCardCmd：:p 的 \_ Nad Nad 方法

\[**Put \_ Nad** 方法可用於 [需求] 區段中指定的作業系統。 它無法用於 Windows Server 2003 Service Pack 1 (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Put \_ Nad** 方法會指定要搭配 [**ISCardCmd**](iscardcmd.md)介面使用 (Nad) 的節點位址。 這僅適用于使用 [*T = 1 通訊協定*](../secgloss/t-gly.md) 通訊的通訊。 根據預設， [**ISCardCmd**](iscardcmd.md) 物件會使用零的 Nad。

## <a name="syntax"></a>語法


```C++
HRESULT put_Nad(
  [in] BYTE bNad
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*bNad* \[在\]
</dt> <dd>

代表要使用之 Nad 的位元組。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | 描述                                      |
|----------------------------------------------------------------------------------------------|--------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業已順利完成。<br/> |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *BNad* 參數無效。<br/>    |



 

## <a name="remarks"></a>備註

只有在需要針對 Nad 使用零以外的值時，才應該呼叫這個方法。

## <a name="examples"></a>範例

下列範例顯示如何指定要搭配 [**ISCardCmd**](iscardcmd.md) 介面使用的節點位址。 此範例假設 byNadValue 是先前已指派值的 **BYTE** 類型變數，而該 PISCardCmd 是 **ISCardCmd** 介面實例的有效指標。


```C++
HRESULT  hr;

// Set the Nad.
// byNadValue is a previously assigned BYTE value.
hr = pISCardCmd->put_Nad(byNadValue);
if (FAILED(hr))
{
  printf("Failed put_Nad\n");
  // Take other error handling action as needed.
}
```



## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|-----------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows\[僅限 XP desktop 應用程式\]<br/>                                             |
| 最低支援的伺服器<br/> | Windows\[僅限 Server 2003 desktop 應用程式\]<br/>                                    |
| 用戶端支援結束<br/>    | Windows XP<br/>                                                                   |
| 伺服器支援結束<br/>    | Windows Server 2003<br/>                                                          |
| 標頭<br/>                   | <dl> <dt>Scarddat。h</dt> </dl>   |
| 類型程式庫<br/>             | <dl> <dt>Scarddat .tlb</dt> </dl> |
| DLL<br/>                      | <dl> <dt>Scardssp.dll</dt> </dl> |
| IID<br/>                      | IID \_ ISCardCmd 定義為 D5778AE3-43DE-11D0-9171-00AA00C18068<br/>            |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[**ISCardCmd**](iscardcmd.md)
</dt> </dl>

 

 
