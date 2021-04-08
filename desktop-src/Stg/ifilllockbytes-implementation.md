---
title: IFillLockBytes-實
description: 系統會提供 IFillLockBytes 的實作為複合檔案執行的一部分。
ms.assetid: a8aed8c5-3c4c-4cce-b568-68031da0edf5
keywords:
- IFillLockBytes Strctd Stg.，執行
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c58737d02e3e6bc2511670178825aef8cbe2dcc0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932183"
---
# <a name="ifilllockbytes---implementation"></a>IFillLockBytes-實

系統會提供 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 的實作為複合檔案執行的一部分。

下載程式代碼可以藉由呼叫 [**StgOpenAsyncDocFileOnIFillLockBytes**](/windows/desktop/api/Objbase/nf-objbase-stgopenasyncdocfileonifilllockbytes)來建立異步複合檔案物件的實例。 下載程式代碼也可以藉由呼叫 [**StgGetIFillLockBytesOnFile**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonfile) 函數或 [**StgGetIFillLockBytesOnILockBytes**](/windows/desktop/api/Objbase/nf-objbase-stggetifilllockbytesonilockbytes) 函數，在現有的檔案或位元組陣列上建立異步位元組陣列包裝函式物件的實例。

## <a name="when-to-use"></a>使用時機

目前，URL 名字標記是 COM 非同步存放裝置執行的唯一使用者。

## <a name="remarks"></a>備註

以下是 [**IFillLockBytes**](/windows/desktop/api/Objidl/nn-objidl-ifilllockbytes) 執行的四個方法。

<dl> <dt>

<span id="IFillLockBytes__FillAppend"></span><span id="ifilllockbytes__fillappend"></span><span id="IFILLLOCKBYTES__FILLAPPEND"></span>**IFillLockBytes::FillAppend**
</dt> <dd>

將新的位元組區塊寫入位元組陣列的結尾。 區塊的大小會指定為 [**FillAppend**](/windows/desktop/api/Objidl/nf-objidl-ifilllockbytes-fillappend)的參數。

</dd> <dt>

<span id="IFillLockBytes__FillAt"></span><span id="ifilllockbytes__fillat"></span><span id="IFILLLOCKBYTES__FILLAT"></span>**IFillLockBytes::FillAt**
</dt> <dd>

將新的資料區塊寫入位元組陣列中的指定位置。

</dd> <dt>

<span id="IFillLockBytes__SetFillSize"></span><span id="ifilllockbytes__setfillsize"></span><span id="IFILLLOCKBYTES__SETFILLSIZE"></span>**IFillLockBytes::SetFillSize**
</dt> <dd>

設定位元組陣列的大小。 \_從呼叫 [**ILockBytes：： ReadAt**](/windows/desktop/api/Objidl/nf-objidl-ilockbytes-readat)傳回 E 失敗，嘗試存取超過方法所指定之上限的資料。

</dd> <dt>

<span id="IFillLockBytes__Terminate"></span><span id="ifilllockbytes__terminate"></span><span id="IFILLLOCKBYTES__TERMINATE"></span>**IFillLockBytes：： Terminate**
</dt> <dd>

通知位元組陣列，已成功或失敗的下載已終止。

</dd> </dl>

 

 




