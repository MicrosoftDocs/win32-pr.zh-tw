---
title: Windows預計的檔案系統詞彙
description: ProjFS 中使用的特殊字詞。
ROBOTS: NOINDEX, NOFOLLOW
ms.assetid: <GUID-GOES-HERE>
ms.date: 01/17/2020
ms.topic: article
ms.openlocfilehash: 12b6e90d98fce3882aa5dc8d552f88e9cd9f389d24673fdc5caf175e180082f2
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120030979"
---
# <a name="windows-projected-file-system-glossary"></a>Windows預計的檔案系統詞彙

ProjFS 中使用的特殊字詞。

<dl>
<dt>

<span id="projfs.glossary_backing_store"></span><span id="PROJFS.GLOSSARY_BACKING_STORE"></span>**備份存放區**
</dt>
<dd>

提供者維護的階層式資料，會以檔案和目錄的形式投射到檔案系統中。
</dd>

<dt>

<span id="projfs.glossary_dirty_placeholder"></span><span id="PROJFS.GLOSSARY_DIRTY_PLACEHOLDER"></span>**中途預留位置**
</dt>
<dd>

已在本機修改過的檔案或目錄，在提供者的存放區中不再是其狀態的快取。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_full_file_directory"></span><span id="PROJFS.GLOSSARY_FULL_FILE_DIRECTORY"></span>**完整檔案/目錄**
</dt>
<dd>

在本機檔案系統中建立的檔案或目錄，或已修改過的檔案，使其不再是備份存放區中其狀態的快取。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_hydrated_placeholder"></span><span id="PROJFS.GLOSSARY_HYDRATED_PLACEHOLDER"></span>**水合預留位置**
</dt>
<dd>

其內容和中繼資料已快取至磁片的檔案。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_placeholder"></span><span id="PROJFS.GLOSSARY_PLACEHOLDER"></span>**占 位 符**
</dt>
<dd>

磁片上未完全存在的檔案或目錄。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_tombstone"></span><span id="PROJFS.GLOSSARY_TOMBSTONE"></span>**墓碑**
</dt>
<dd>

表示已從本機檔案系統刪除之專案的特殊隱藏預留位置。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_virtual_file_directory"></span><span id="PROJFS.GLOSSARY_virtual_file_directory"></span>**虛擬檔案/目錄**
</dt>
<dd>

未實際存在於磁片上的檔案或目錄，但投射到列舉結果。  請參閱 [虛擬化根中的](cache-state.md)快取狀態。
</dd>

<dt>

<span id="projfs.glossary_virtualization_instance"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_INSTANCE"></span>**虛擬化實例**
</dt>
<dd>

記憶體中的物件，可管理位於特定虛擬根目錄下之檔案和目錄集合的提供者與 ProjFS 之間的通訊。
</dd>

<dt>

<span id="projfs.glossary_virtualization_root"></span><span id="PROJFS.GLOSSARY_VIRTUALIZATION_ROOT"></span>**虛擬化根**
</dt>
<dd>

檔案系統中用來投射提供者資料的目錄。
</dd>

</dl>

<!--
<dt>

<span id="projfs.glossary_"></span><span id="PROJFS.GLOSSARY_"></span>**TERM**
</dt>
<dd>

DEFINITION
</dd>
-->