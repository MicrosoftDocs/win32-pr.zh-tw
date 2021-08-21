---
description: 深入瞭解：可擴充的儲存體引擎
title: 可擴充的儲存體引擎
TOCTitle: Extensible Storage Engine
ms:assetid: 5c485eff-4329-4dc1-aa45-fb66e6554792
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269259(v=EXCHG.10)
ms:contentKeyID: 32765561
ms.date: 04/11/2016
ms.topic: article
ms.openlocfilehash: d1ec139cf947cb2d95bfccf3737c1f6559bf01ffbfa55f2e9a7d1e890efd6a3d
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118980818"
---
# <a name="extensible-storage-engine"></a>可擴充的儲存體引擎


_**適用于：** Windows |Windows伺服器_

## <a name="extensible-storage-engine"></a>可擴充的儲存體引擎

可延伸的儲存體引擎 (ESE) 是 (ISAM) 儲存體技術的先進索引和循序存取方法。 ESE 可讓應用程式使用索引或連續資料指標流覽來儲存和取出資料表中的資料。 它支援反正規化的架構，包括具有多個稀疏資料行的寬型資料表、多重值資料行，以及稀疏和豐富的索引。 它可讓應用程式使用交易資料更新和抓取來享受一致的資料狀態。 系統會提供損毀復原機制，以在發生系統損毀時維持資料一致性。 它透過預先寫入記錄檔和快照集隔離模型，透過資料和架構來提供 ACID (不可部分完成的一致隔離持久) 交易。 ESE 中的交易高度並行，讓 ESE 適用于伺服器應用程式。 它會快取資料，以最大化高效能存取資料。 此外，它也很輕量，適用于輔助角色中提供的應用程式。

ESE 適用于需要快速和/或輕量結構化資料儲存體的應用程式，其中原始檔案存取或登錄不支援應用程式的索引編制或資料大小需求。

它是由應用程式所使用，而且永遠不會儲存超過 1 mb 的資料，而且已用於具有資料庫的應用程式（在極端情況下超過 1 tb，且通常超過 50 gb）。

本檔適用于熟悉 C 和 c + + 的開發人員，以及基本的資料庫概念，例如資料表、資料行、索引、復原和交易。 ESE 的唯一存取方法是此檔中所述的 C API。

可擴充的儲存體引擎是 Windows 2000 中引進的 Windows 元件。 並非所有的功能或 api 都適用于所有版本的 Windows 作業系統。

ESE 提供使用者模式儲存引擎，可管理可透過 Windows api 存取之一般二進位檔案內的資料。 ESE 可透過直接載入至應用程式進程的 DLL 來存取;資料庫引擎本身不需要或提供任何遠端存取方法。 雖然 ESE 沒有遠端或進程間的存取方法，但是它所使用的資料檔案可透過 Windows api (SMB) 從遠端提供，但不建議這麼做。

**注意** Windows XP 64 位版本與 Windows Server 2003 相同，目的是要判斷所支援的 ESE 功能集。  

### <a name="notes"></a>備註

ESE 先前稱為聯合引擎技術 (JET) Blue，因此通常會將「JET Blue」或「JET」這一詞與本檔以外的 ESE 一詞一起使用。 但事實上，JET API 有兩個完全不同的執行方式，稱為 JET Blue 和 JET Red。 「jet」一詞經常用來指的是 jet Red，也就是與 Microsoft Office 存取搭配使用的 database engine。 這兩個 JET 執行完全不同、個別維護、具有極大不同的功能集，且不可互換。 在 ESE 檔中，「JET」指的是 ESE 或 JET API，因為 ESE 會執行它。 任何對 JET Red 的參考永遠都會明確標示為「JET Red」。

### <a name="in-this-section"></a>本節內容

[可擴充的儲存體引擎參考](./extensible-storage-engine-reference.md)
