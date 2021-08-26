---
description: 捕獲 NPP 狀態。
ms.assetid: 48682997-f641-4ae5-b5ad-64fd84f07ae3
title: 'IESP：： QueryStatus 方法 (Netmon. h) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- IESP.QueryStatus
api_type:
- COM
api_location:
- Ndisnpp.dll
- Rmtnpp.dll
ms.openlocfilehash: 00b83cbbb167775a8de360c880f381b41f250abf0eab01c883bc7580be4d956f
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120037538"
---
# <a name="iespquerystatus-method"></a>IESP：： QueryStatus 方法

**QueryStatus** 方法會捕獲 NPP 狀態。

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

傳回之 >networkstatus 結構的指標，指出目前狀態 (在 NPP 的) 上進行的[](networkstatus.md) 、暫停、停止等等。 使用者必須配置和釋放 >NETWORKSTATUS 結構的記憶體。

</dd> </dl>

## <a name="return-value"></a>傳回值

如果方法成功，則傳回值為 NMERR \_ SUCCESS。

如果此方法不成功，則傳回值會是下列錯誤碼：



| 傳回碼                                                                                              | 描述                                                                                                                                                                                 |
|----------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <dl> <dt>**NMERR \_ 不正確 \_ 參數**</dt> </dl> | *PNetworkStatus* 參數未指向有效的 [>networkstatus](networkstatus.md)結構。 配置此結構的記憶體，並再次呼叫 **IESP：： QueryStatus** 。<br/> |



 

## <a name="remarks"></a>備註

呼叫 [CreateNPPInterface](createnppinterface.md) 之後，隨時都可以呼叫這個方法。 您可以呼叫這個方法來查看 NPP 是否已連接到網路、找出目前的捕獲狀態，以及查看是否有任何觸發程式暫止。

在呼叫這個方法之前，請先配置 [>networkstatus](networkstatus.md) 結構所需的記憶體，並在不再需要該結構時釋放該記憶體。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------|
| 最低支援的用戶端<br/> | Windows 2000 Professional \[僅限傳統型應用程式\]<br/>                                                                                               |
| 最低支援的伺服器<br/> | Windows 2000 Server \[僅限傳統型應用程式\]<br/>                                                                                                     |
| 標頭<br/>                   | <dl> <dt>Netmon</dt> </dl>                                                                      |
| DLL<br/>                      | <dl> <dt>Ndisnpp.dll;</dt><dt>Rmtnpp.dll</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[IESP](iesp.md)
</dt> <dt>

[CreateNPPInterface](createnppinterface.md)
</dt> <dt>

[>NETWORKSTATUS](networkstatus.md)
</dt> </dl>

 

 




