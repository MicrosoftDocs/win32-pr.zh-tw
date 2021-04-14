---
title: ILockBytes-File-Based 執行
description: 在 COM 複合檔案儲存物件基礎的位元組陣列物件上執行，並設計成直接讀取和寫入磁片檔案。
ms.assetid: 700b6a3c-1046-4c21-8887-16f344c23510
keywords:
- ILockBytes Strctd Stg.，以檔案為基礎
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 93dfe09ab0157d2d24d81b7bb2798e984d3848f4
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104371937"
---
# <a name="ilockbytes---file-based-implementation"></a>ILockBytes-File-Based 執行

在 COM 複合檔案儲存物件基礎的位元組陣列物件上執行，並設計成直接讀取和寫入磁片檔案。

## <a name="when-to-use"></a>使用時機

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)的方法是從透過呼叫 [**StgCreateDocfile**](/windows/desktop/api/coml2api/nf-coml2api-stgcreatedocfile)所建立的複合檔案儲存物件上 [**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)和 [**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)的複合檔案執行所呼叫，因此您不需要直接呼叫它們。

## <a name="remarks"></a>備註

以下是 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) File-Based 執行的方法。

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

確保 [**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes) 執行所維護的任何內部緩衝區都會寫出到基礎實體儲存體。

</dd> <dt>

<span id="ILockBytes__SetSize"></span><span id="ilockbytes__setsize"></span><span id="ILOCKBYTES__SETSIZE"></span>**ILockBytes：： SetSize**
</dt> <dd>

設定位元組陣列的大小。

</dd> <dt>

<span id="ILockBytes__LockRegion"></span><span id="ilockbytes__lockregion"></span><span id="ILOCKBYTES__LOCKREGION"></span>**ILockBytes：： LockRegion**
</dt> <dd>

*DwLockTypes* 參數設定為 lock \_ ONLYONCE 或 \_ 獨佔鎖定，可允許或限制對鎖定區域的存取。

</dd> <dt>

<span id="ILockBytes__UnlockRegion"></span><span id="ilockbytes__unlockregion"></span><span id="ILOCKBYTES__UNLOCKREGION"></span>**ILockBytes：： UnlockRegion**
</dt> <dd>

這個方法會將 [**ILockBytes：： LockRegion**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-lockregion)鎖定的區域解除鎖定。

</dd> <dt>

<span id="ILockBytes__Stat"></span><span id="ilockbytes__stat"></span><span id="ILOCKBYTES__STAT"></span>**ILockBytes：： Stat**
</dt> <dd>

COM 提供的 [**IStorage：： stat**](/windows/desktop/api/Objidl/nf-objidl-istorage-stat) 實，會呼叫 [**ILockBytes：： stat**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-stat) 方法，以取得位元組陣列物件的相關資訊。 如果位元組陣列沒有合理的名稱，則 COM 提供的 **ILockBytes：： Stat** 方法會在 [**STATSTG**](/windows/win32/api/objidl/ns-objidl-statstg)結構的 **pwcsName** 成員中傳回 **Null** 。

</dd> </dl>

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**ILockBytes**](/windows/desktop/api/Objidl/nn-objidl-ilockbytes)
</dt> <dt>

[**IStorage**](/windows/desktop/api/Objidl/nn-objidl-istorage)
</dt> <dt>

[**IStream**](/windows/desktop/api/Objidl/nn-objidl-istream)
</dt> </dl>

 

 




