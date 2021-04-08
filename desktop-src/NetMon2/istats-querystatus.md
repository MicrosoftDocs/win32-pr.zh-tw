---
description: QueryStatus 方法會捕獲 NPP 的狀態。
ms.assetid: 86b1c1ee-3a35-4603-9e93-fe09f886c32f
title: 'IStats：： QueryStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IStats.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 02e013d87734b61ad26b6563c402db1b8d4cb4f7
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103695867"
---
# <a name="istatsquerystatus-method"></a>IStats：： QueryStatus 方法

**QueryStatus** 方法會捕獲 NPP 的狀態。

## <a name="syntax"></a>語法


```C++
HRESULT STDMETHODCALLTYPE QueryStatus(
  [out] NETWORKSTATUS *pNetworkStatus
);
```



## <a name="parameters"></a>參數

<dl> <dt>

*pNetworkStatus* \[擴展\]
</dt> <dd>

傳回之 >networkstatus 結構的指標，指出目前狀態 (在 NPP 的) 上進行的[](networkstatus.md) 、暫停、停止等等。 應用程式必須負責配置和釋放 **>networkstatus** 結構的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值會是下列錯誤碼：



| 傳回碼                                                                                              | Description                                                                                                                                                                                              |
|----------------------------------------------------------------------------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 不正確 \_ 參數**</dt> </dl> | *PNetworkStatus* 參數未指向有效的 [>networkstatus](networkstatus.md)結構。 配置此結構的記憶體，並再次呼叫 **IStats：： QueryStatus** 方法。<br/> |



 

## <a name="remarks"></a>備註

呼叫 [CreateNPPInterface](createnppinterface.md) 方法之後，隨時都可以呼叫這個方法。 您可以呼叫它來查看 NPP 是否已連線到網路、找出目前的捕獲狀態，以及查看是否有任何觸發程式暫止。 不過，在呼叫這個方法之前，您必須先配置 [>networkstatus](networkstatus.md) 結構所需的記憶體，並在不再需要該結構時釋放該記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IStats](istats.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[>NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




