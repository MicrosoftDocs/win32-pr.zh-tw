---
title: ILockBytes-全域記憶體執行
description: ILockBytes global memory 實作為 COM 複合檔案儲存物件基礎的位元組陣列物件，並設計為可直接讀取和寫入全域記憶體。
ms.assetid: 6ab019b0-34d7-4b6e-ba77-6b6881fabd29
keywords:
- ILockBytes Strctd Stg.、、global memory
- ILockBytes Strctd Stg.，實施
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e9d7cae82c1503fcb53d2cfd8fee39095eb60801
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300311"
---
# <a name="ilockbytes---global-memory-implementation"></a>ILockBytes-全域記憶體執行

ILockBytes global memory 實作為 COM 複合檔案儲存物件基礎的位元組陣列物件，並設計為可直接讀取和寫入全域記憶體。

## <a name="when-to-use"></a>使用時機

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)的方法是從透過呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)所建立的複合檔案儲存物件上， [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行所呼叫。

## <a name="remarks"></a>備註

以下是 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) Global Memory 執行的方法。

<dl> <dt>

<span id="ILockBytes__ReadAt"></span><span id="ilockbytes__readat"></span><span id="ILOCKBYTES__READAT"></span>**ILockBytes：： ReadAt**
</dt> <dd>

從位元組陣列開頭的指定位移讀取位元組區塊。

</dd> <dt>

<span id="ILockBytes__WriteAt"></span><span id="ilockbytes__writeat"></span><span id="ILOCKBYTES__WRITEAT"></span>**ILockBytes：： WriteAt**
</dt> <dd>

從位元組陣列開頭的指定位移寫入位元組區塊。

</dd> <dt>

<span id="ILockBytes__Flush"></span><span id="ilockbytes__flush"></span><span id="ILOCKBYTES__FLUSH"></span>**ILockBytes：： Flush**
</dt> <dd>

不同于以檔案為基礎的執行，在全域記憶體執行中呼叫這個方法沒有任何作用。

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes：： SetSize**
</dt> <dd>

設定位元組陣列的大小。

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes：： LockRegion**
</dt> <dd>

這項執行不支援鎖定，所以 *dwLocksType* 會設定為零。 呼叫端必須確定存取有效且互斥。

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes：： UnlockRegion**
</dt> <dd>

這種執行不支援鎖定。

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes：： Stat**
</dt> <dd>

COM 提供的 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) 實，會呼叫 [**ILockBytes：： stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) 方法來取出位元組陣列物件的相關資料。 如果位元組陣列沒有合理的名稱，則 COM 提供的 **ILockBytes：： Stat** 方法會在 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg)結構的 **pwcsName** 成員中傳回 **Null** 。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




