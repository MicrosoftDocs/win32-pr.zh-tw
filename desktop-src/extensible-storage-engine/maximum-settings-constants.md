---
description: 深入瞭解：最大設定常數
title: 最大設定常數
TOCTitle: Maximum Settings Constants
ms:assetid: 1111051f-55af-4c33-be38-6a3973c2c815
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269189(v=EXCHG.10)
ms:contentKeyID: 32765492
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
ms.openlocfilehash: 38184176e5803cfd22d7b63f9d85e5b62f7ecff1
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122478964"
---
# <a name="maximum-settings-constants"></a>最大設定常數


_**適用于：** Windows |Windows伺服器_

## <a name="maximum-settings-constants"></a>最大設定常數

這些常數會提供 ESE 資料庫中專案上所允許的最大設定。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_BASE_NAME_LENGTH<br />3</p> | <p>設定用來命名資料庫引擎所使用之檔案的前置詞長度。 此長度適用于為 <a href="gg269235(v=exchg.10).md">JET_paramBaseName</a> 系統參數設定的名稱。</p> | 
| <p>JET_MAX_COMPUTERNAME_LENGTH<br />15</p> | <p>設定 <a href="gg269340(v=exchg.10).md">JET_SIGNATURE</a>的最大長度。</p> | 
| <p>JET_cbBookmarkMost<br />256</p> | <p>書簽的預設大小上限。 當金鑰大小保留為其預設值時，這會是有效的。</p> | 
| <p>JET_cbBookmarkMostMost<br />2000</p> | <p>當 esent 設定為具有最大的可用索引鍵時，書簽的大小上限。</p><p><strong>Windows 7：</strong>JET_cbBookmarkMostMost 會在 Windows 7 中引進。</p> | 
| <p>JET_cbNameMost<br />64</p> | <p>物件、資料行、索引或屬性名稱的最大長度。</p><p><strong>注意</strong>  若為 Unicode，則值為128。</p> | 
| <p>JET_cbFullNameMost<br />255</p> | <p>"Name.name.name ..." 的最大長度構建。</p><p><strong>注意</strong>  若為 Unicode，則值為510。</p> | 
| <p>JET_cbColumnLVPageOverhead<br />82</p> | <p>此數位可用來計算資料庫引擎可在單一資料庫頁面上儲存之 BLOB 的最大數量。 公式的大小上限 = JET_paramDatabasePageSize – JET_cbColumnLVPageOverhead。</p><p>此值現在已過時。 應該使用 JET_paramLVChunkSizeMost 參數來取出長值的區塊大小。</p> | 
| <p>JET_cbColumnMost<br />255</p> | <p>非 long 值資料行資料的大小上限。</p> | 
| <p>JET_cbLVDefaultValueMost<br />255</p> | <p>長值 (LongBinary 或 LongText) 資料行預設值的大小上限。</p> | 
| <p>JET_cbKeyMost<br />255</p> | <p>排序或索引鍵的預設大小上限。</p> | 
| <p>JET_cbKeyMostMost<br />2000</p> | <p>任何頁面大小之排序或索引鍵可設定的最大大小。  (參閱 JET_INDEXCREATE2 cbKeyMost) </p><p><strong>Windows 7：</strong>JET_cbKeyMostMost 是在 Windows 7 作業系統中引進。</p> | 
| <p>JET_cbKeyMost2KBytePage<br />500</p> | <p>使用2048位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p><p><strong>Windows Vista：</strong>JET_cbKeyMost2KBytePage 是 Windows Vista 作業系統引進的。</p> | 
| <p>JET_cbKeyMost4KBytePage<br />1000</p> | <p>使用4096位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p><p><strong>Windows Vista：</strong>JET_cbKeyMost4KBytePage 是 Windows Vista 引進。</p> | 
| <p>JET_cbKeyMost8KBytePage<br />2000</p> | <p>使用8192位元組頁面的資料庫中，最大允許的索引鍵可設定的大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p><p><strong>Windows Vista：</strong>Windows Vista 引進 JET_cbKeyMost8KBytePage</p> | 
| <p>JET_cbKeyMostMin<br />255</p> | <p>索引鍵的最小允許大小上限。 如需詳細資訊，請參閱 <a href="gg269186(v=exchg.10).md">JET_INDEXCREATE</a> 。</p><p><strong>Windows Vista：</strong>JET_cbKeyMostMin 是 Windows Vista 引進。</p> | 
| <p>JET_cbLimitKeyMost<br />256</p> | <p>使用限制 <em>grbit</em>（例如在 <a href="gg269329(v=exchg.10).md">JetMakeKey</a> 函數中使用的 JET_bitStrLimit）來形成索引鍵時的最大索引鍵大小。</p> | 
| <p>JET_cbPrimaryKeyMost<br />255</p> | <p>主要索引的大小上限。 這項功能現在已過時。</p> | 
| <p>JET_cbSecondaryKeyMost<br />255</p> | <p>次要索引的大小上限。 這項功能現在已過時。</p> | 
| <p>JET_ccolKeyMost<br />12</p> | <p>排序或索引鍵中元件的最大數目。</p><p><strong>Windows Vista：</strong>在 Windows Vista 和更新版本的 Windows 值為16。</p> | 
| <p>JET_ccolMost<br />0x0000fee0</p> | <p>資料表中允許的資料行數目上限。</p><p><strong>Windows XP：</strong>值0x0000fee0 用於 Windows XP 及更新版本和更新版本的 Windows</p><p><strong>Windows 2000：</strong>值0x00007ffe 用於 Windows 2000。</p> | 
| <p>JET_ccolFixedMost<br />0x0000007f</p> | <p>資料表中允許的固定資料行數目上限（目前為127）。</p> | 
| <p>JET_ccolVarMost<br />0x00000080</p> | <p>可包含在資料表中之可變長度資料行的最大數目，目前為128。</p> | 
| <p>JET_ccolTaggedMost<br /> ( JET_ccolMost 0x000000ff ) </p> | <p>可包含在資料表中的標記資料行數目上限，目前為64993。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


