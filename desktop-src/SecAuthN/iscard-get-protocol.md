---
description: 抓取智慧卡上目前正在使用的通訊協定識別碼。
ms.assetid: 68c75e98-da5c-4e3e-9836-369941751fb0
title: 'ISCard：： get_Protocol 方法 (Scardmgr .h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- ISCard.get_Protocol
api_type:
- COM
api_location:
- Scardssp.dll
ms.openlocfilehash: fb58f890da85e3348ede6af70a006f98daac38a1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104320196"
---
# <a name="iscardget_protocol-method"></a>ISCard：： get \_ 通訊協定方法

\[**取得 \_ 通訊協定** 方法可用於 [需求] 區段中指定的作業系統。 它無法在 Windows Server 2003 （含 Service Pack 1） (SP1) 和更新版本、Windows Vista、Windows Server 2008 和後續版本的作業系統中使用。 [智慧卡模組](/previous-versions/windows/desktop/secsmart/smart-card-modules)提供類似的功能。\]

**Get \_ 通訊協定** 方法會抓取 [*智慧卡*](../secgloss/s-gly.md)上目前正在使用的通訊協定識別碼。

## <a name="syntax"></a>語法


```C++
HRESULT get_Protocol(
  [out] SCARD_PROTOCOLS *pProtocol
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pProtocol* \[擴展\]
</dt> <dd>

通訊協定識別碼的指標。

</dd> </dl>

## <a name="return-value"></a>傳回值

方法會傳回下列其中一個可能的值。



| 傳回碼                                                                                  | Description                                         |
|----------------------------------------------------------------------------------------------|-----------------------------------------------------|
| <dl> <dt>**S \_ 確定**</dt> </dl>         | 作業順利完成。<br/>        |
| <dl> <dt>**E \_ INVALIDARG**</dt> </dl> | *PProtocol* 參數無效。<br/>  |
| <dl> <dt>**E \_ 指標**</dt> </dl>    | 在 *pProtocol* 中傳遞了錯誤指標。<br/> |



 

## <a name="remarks"></a>備註

除了上面所列的 COM 錯誤碼之外，如果呼叫智慧卡函式來完成要求，此介面可能會傳回智慧卡的錯誤碼。 如需詳細資訊，請參閱 [智慧卡傳回值](authentication-return-values.md)。

## <a name="examples"></a>範例

下列範例顯示如何抓取智慧卡上目前正在使用的通訊協定識別碼。


```C++
SCARD_PROTOCOLS   scProtocol;
HRESULT           hr;

// Retrieve the protocol.
hr = pISCard->get_Protocol(&scProtocol);
if (FAILED(hr))
{
   printf("Failed get_Protocol\n");
   // Take other error handling action as needed.
}
// Use the retrieved protocol. (This example merely displays it.)
switch (scProtocol)
{
    case T0:
        printf("T0 protocol\n");
        break;
    case T1:
        printf("T1 protocol\n");
        break;
    default:
        printf("Other protocol\n");
        break;
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

[**取得 \_ Atr**](iscard-get-atr.md)
</dt> <dt>

[**取得 \_ CardHandle**](iscard-get-cardhandle.md)
</dt> <dt>

[**取得 \_ 內容**](iscard-get-context.md)
</dt> <dt>

[**取得 \_ 狀態**](iscard-get-status.md)
</dt> <dt>

[**ISCard**](iscard.md)
</dt> </dl>

 

 
