---
description: 請注意，這個 API 已被取代。 新的應用程式不應使用它。 MSPID 資料類型可識別媒體資料流程的用途。
ms.assetid: 83a84eb7-a72c-4ca7-b152-8cc81a5bfdaf
title: 'MSPID (Mmstream) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 8464882aa018a373345f15c0a5639107d9beebf9
ms.sourcegitcommit: c8ec1ded1ffffc364d3c4f560bb2171da0dc5040
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/22/2021
ms.locfileid: "106984364"
---
# <a name="mspid"></a>MSPID

> [!Note]  
> 此 API 即將淘汰。 新的應用程式不應使用它。

 

**MSPID** 資料類型可識別媒體資料流程的用途。


```C++
typedef GUID MSPID;
typedef REFGUID REFMSPID;
```



## <a name="remarks"></a>備註

**MSPID** 只是 GUID 的 typedef。 已定義下列 MSPIDs。



| 值               | 描述           |
|---------------------|-----------------------|
| MSPID \_ PrimaryVideo | 主要影片串流。 |
| MSPID \_ PrimaryAudio | 主要音訊串流。 |



 

**REFMSPID** 型別會定義 **MSPID** 的參考。

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|-------------------|---------------------------------------------------------------------------------------|
| 標頭<br/> | <dl> <dt>Mmstream。h</dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[多媒體串流資料類型](multimedia-streaming-data-types.md)
</dt> </dl>

 

 




