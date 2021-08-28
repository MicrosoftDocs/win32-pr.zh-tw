---
description: 深入瞭解： JET_SPACEHINTS 結構
title: JET_SPACEHINTS 結構
TOCTitle: JET_SPACEHINTS Structure
ms:assetid: 23328993-93c9-4a23-892b-e6a9f434d1d6
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269205(v=EXCHG.10)
ms:contentKeyID: 32765508
ms.date: 04/11/2016
ms.topic: reference
api_name: ''
topic_type:
- apiref
- kbArticle
api_type:
- COM
api_location: ''
ROBOTS: INDEX,FOLLOW
ms.openlocfilehash: 77c452fb78916fdcdf935ec6ad890db055e63b9a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122479314"
---
# <a name="jet_spacehints-structure"></a>JET_SPACEHINTS 結構


_**適用于：** Windows |Windows伺服器_

## <a name="jet_spacehints-structure"></a>JET_SPACEHINTS 結構

當 b 型樹狀結構透過附加或 hotpoint 分割成長時， **JET_SPACEHINTS** 結構包含空間配置模式的相關資訊。 當將記錄加入 b 型樹狀目錄的結尾，並在多筆記錄新增至相同的虛擬插入點時，就會發生 hotpoint 分割 (例如，將 ' Marie '、' Mark '、' Martin'，' Mary ' 加入到依字母) 順序排序的 b 型樹狀目錄中間。

**Windows 7：** Windows 7 中引進 **JET_SPACEHINTS** 結構。

```cpp
    typedef struct tagJET_SPACEHINTS {
      unsigned long cbStruct;
      unsigned long ulInitialDensity;
      unsigned long cbInitial;
      JET_GRBIT grbit;
      unsigned long ulMaintDensity;
      unsigned long ulGrowth;
      unsigned long cbMinExtent;
      unsigned long cbMaxExtent;
    } JET_SPACEHINTS;
```

### <a name="members"></a>成員

**cbStruct**

此結構的大小（以位元組為單位）。 將這個成員設定為 sizeof ( JET_SPACEHINTS ) 。

**ulInitialDensity**

 (的密度會附加) 版面配置。

**cbInitial**

所建立之物件的初始大小 (位元組) 。 這必須是資料庫頁面大小的倍數。

**grbit**

位群組，其中包含要用於此結構的選項，包括下列零或多個。


| <p>值</p> | <p>意義</p> | 
|--------------|----------------|
| <p>JET_bitSpaceHintsUtilizeParentSpace<br />0x00000001</p> | <p>變更內部配置原則，以從 b 型樹狀目錄的直屬父系取得空間 heirarchically。</p> | 
| <p>JET_bitCreateHintAppendSequential<br />0x00000002</p> | <p>根據 cbMinExtent、ulGrowth、cbMaxExtent) 所設定的 (資料表成長動態，讓附加分割行為成長。</p> | 
| <p>JET_bitCreateHintHotpointSequential<br />0x00000004</p> | <p>根據 cbMinExtent、ulGrowth、cbMaxExtent) 所設定之資料表 (成長動態，讓 hotpoint 分割行為成長。</p> | 
| <p>JET_bitRetrieveHintTableScanForward<br />0x00000010</p> | <p>如果設定，用戶端會指出向前順序掃描是此資料表的主要使用模式。</p> | 
| <p>JET_bitRetrieveHintTableScanBackward<br />0x00000020</p> | <p>如果設定，用戶端就會指出往後順序掃描是此資料表的主要使用模式。</p> | 
| <p>JET_bitDeleteHintTableSequential<br />0x00000100</p> | <p>如果設定，應用程式預期會依序從最小的索引鍵到最高的索引鍵來清除此資料表。</p> | 



**ulMaintDensity**

密度至 mulMaintDensity

要維護的密度。 如果空間提示指定 JET_bitRetrieveHintTableScanForward 或 JET_bitRetrieveHintTableScanBackward，當資料表中的已使用空間低於此臨界值時，就會觸發資料表磁碟重組。 您可以將此成員設定為零，以停用資料表磁碟重組。 將這個成員設定為100，將會在釋放頁面時立即執行資料表磁碟重組。

**ulGrowth**

從上一次成長或初始大小的成長百分比，舍入到最接近的原生 JET 配置大小。

**cbMinExtent 太小**

如果太小，則會覆寫 ulGrowth。

**cbMaxExtent**

成長的最大值（以位元組為單位）。 此 cap ulGrowth。

### <a name="when-a-b-tree-grows-through-append-or-hotpoint-splits-as-opposed-to-random-record-insertions-the-amount-of-space-the-table-will-grow-by-is-calculated-as-follows"></a>當 b 型樹狀結構透過附加或 hotpoint 分割 (而不是隨機記錄插入) 時，資料表將成長的空間量計算方式如下：

1.  在建立過程中，我們會為 b 型樹狀結構 cbInitial，一律為。

2.  在指定區域的第一次配置期間，我們將配置： cbInitial \* ulGrowth/100 (四捨五入至 DB 的頁面大小) ，或 cbMinExtent （如果較大）。

3.  在下一個配置期間，cbLastAlloc \* ulGrowth/100 (舍入至資料庫) 的頁面大小，如果較大則為 cbMinExtent。

4.  在某些配置 (可能是第一次配置) 時，計算的大小會超過 cbMaxExtent，而這會是之後的成長大小。

### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_TABLECREATE2](./jet-tablecreate2-structure.md)  
[JET_TABLECREATE3](./jet-tablecreate3-structure.md)
