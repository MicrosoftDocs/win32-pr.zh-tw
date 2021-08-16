---
description: CCritSec 類別提供執行緒鎖定。
ms.assetid: ecc60afe-15d0-4780-8133-1dfc558c6325
title: 'CCritSec 類別 (Wxutil) '
ms.topic: reference
ms.date: 05/31/2018
topic_type:
- APIRef
- kbSyntax
api_name:
- CCritSec
api_type:
- COM
api_location:
- Strmbase.lib
- Strmbase.dll
- Strmbasd.lib
- Strmbasd.dll
ms.openlocfilehash: eb57004935a85392057120c0ec369d19217148780079ab4be83088dd3de3ea8d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119872188"
---
# <a name="ccritsec-class"></a>CCritSec 類別

**CCritSec** 類別提供執行緒鎖定。

這個類別是 Windows **重要 \_ 區段** 物件的精簡型包裝函式。 您可以藉由呼叫 [**CCritSec：： lock**](ccritsec-lock.md) 和 [**CCritSec：： unlock**](ccritsec-unlock.md) 方法來鎖定和解除鎖定執行緒。 但是，將此類別與 [**CAutoLock**](cautolock.md) 類別搭配使用會比較安全。 當 **CAutoLock** 類別超出範圍時，會自動將 **CCritSec** 物件解除鎖定。 此外，它也會編譯成有效率的內嵌程式碼。



| Public 成員變數                            | Description                                              |
|----------------------------------------------------|----------------------------------------------------------|
| [**m \_ currentOwner**](ccritsec-m-currentowner.md) | 擁有線程的執行緒識別碼。                  |
| [**m \_ lockCount**](ccritsec-m-lockcount.md)       | 此物件上的未完成鎖定數目。              |
| [**m \_ fTrace**](ccritsec-m-ftrace.md)             | 指定是否要追蹤此鎖定的布林值。 |
| 公用方法                                     | Description                                              |
| [**CCritSec**](ccritsec-ccritsec.md)              | 函式方法。                                      |
| [**~ CCritSec**](ccritsec--ccritsec.md)            | 函式方法。                                       |
| [**鎖定**](ccritsec-lock.md)                      | 鎖定重要區段物件。                       |
| [**Unlock**](ccritsec-unlock.md)                  | 解除鎖定重要區段物件。                     |



 

## <a name="requirements"></a>規格需求



| 需求 | 值 |
|--------------------|--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 標頭<br/>  | <dl> <dt>Wxutil (包含： .h) </dt> </dl>                                                                                    |
| 程式庫<br/> | <dl> <dt> (零售組建的 Strmbase .lib) ;</dt><dt>Strmbasd (debug 組建) </dt> </dl> |



## <a name="see-also"></a>另請參閱

<dl> <dt>

[重要區段物件](/windows/desktop/Sync/critical-section-objects)
</dt> <dt>

[DirectShow基類參考](base-class-reference.md)
</dt> </dl>

 

