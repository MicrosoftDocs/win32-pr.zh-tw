---
description: 深入瞭解： JET_COLTYP
title: JET_COLTYP
TOCTitle: JET_COLTYP
ms:assetid: 2c30c025-629d-4b94-bcb9-9c8fc3d4e039
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269213(v=EXCHG.10)
ms:contentKeyID: 32765516
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
ms.openlocfilehash: dfe7a12284c6144d9eca0b3e320f43e68ea66b4d
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122985271"
---
# <a name="jet_coltyp"></a>JET_COLTYP


_**適用于：** Windows |Windows伺服器_

## <a name="jet_coltyp"></a>JET_COLTYP

**JET_COLTYP** 的常數群組描述可在資料表中找到的所有可能資料行類型。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_coltypNil<br />0</p> | <p>不正確資料行類型。</p> | 
| <p>JET_coltypBit<br />1</p> | <p>允許三個值的資料行類型： <strong>True</strong>、 <strong>False</strong>或 <strong>Null</strong>。 這種類型的資料行是長度的一個位元組，而且是固定的大小。 <strong>False</strong> 會在 <strong>True</strong>之前排序。 請注意，這個類型的大小不符合 variant 布林值類型的大小。</p> | 
| <p>JET_coltypUnsignedByte<br />2</p> | <p>1位元組不帶正負號的整數，可採用 0 (零) 和255之間的值。</p> | 
| <p>JET_coltypShort<br />3</p> | <p>2位元組帶正負號的整數，可採用-32768 和32767之間的值。 負數值會在正值之前排序。</p> | 
| <p>JET_coltypLong<br />4</p> | <p>4位元組帶正負號的整數，可採用-2147483648 和2147483647之間的值。 負數值會在正值之前排序。</p> | 
| <p>JET_coltypCurrency<br />5</p> | <p>8位元組帶正負號的整數，可採用-9223372036854775808 和9223372036854775807之間的值。 負數值會在正值之前排序。 此資料行類型與 variant 貨幣類型相同。 此資料行類型也可以用來當做原生8位元組帶正負號的整數。</p> | 
| <p>JET_coltypIEEESingle<br />6</p> | <p>單精確度 (4 位元組) 浮點數。</p> | 
| <p>JET_coltypIEEEDouble<br />7</p> | <p>雙精確度 (8 位元組的) 浮點數。</p> | 
| <p>JET_coltypDateTime<br />8</p> | <p>雙精確度 (8 位元組) 浮點數，表示自1900年起算的日期（以小數天為單位）。 此資料行類型與 variant 日期類型相同。</p> | 
| <p>JET_coltypBinary<br />9</p> | <p>固定或可變長度的原始二進位資料行，長度最多可達255個位元組。</p><p>如果設定為固定長度的16位元組二進位資料行，此資料行類型可以用來執行 GUID。 唯一要注意的是，在這類資料行的索引中，值的相對順序，不會比對 GUID (之標準登錄字串轉譯的相對順序，也就是 "{0d6cec99-3f3f-4dc7-a5e6-f87aefeb908b}" ) 。</p> | 
| <p>JET_coltypText<br />10</p> | <p>固定或可變長度的文字資料行，長度最多可達255個 ASCII 字元或127個 Unicode 字元。</p><p>所有字串都會儲存為計數的字元數。 字串不需要是以 null 結束。 此外，count 不需要包含 null 結束字元。 最後，可以儲存內嵌的 null 字元。</p><p>針對排序和搜尋用途，系統一律會將 ASCII 字串視為不區分大小寫。 此外，如果有任何) 被視為排序和搜尋，則只有第一個 null 字元前面的字元 (。</p><p>Unicode 字串會使用 WIN32 API <a href="/windows/win32/api/winnls/nf-winnls-lcmapstringa">LCMapString</a> 來建立排序索引鍵，之後用來排序和搜尋該資料。 根據預設，Unicode 字串會被視為美國英文地區設定，並使用下列正規化旗標進行排序和搜尋： NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。 在 Windows 2000 中，您可以自訂每個索引的這些旗標，以同時包含 NORM_IGNORENONSPACE。 在 Windows XP 和更新版本中，可以為每個索引要求下列正規化旗標的任意組合： LCMAP_SORTKEY、LCMAP_BYTEREV、NORM_IGNORECASE、NORM_IGNORENONSPACE、NORM_IGNORESYMBOLS、NORM_IGNOREKANATYPE、NORM_IGNOREWIDTH 和 SORT_STRINGSORT。</p><p>在所有版本中，都可以自訂每個索引的地區設定。 只要電腦上已安裝適當的語言套件，即可使用任何地區設定。 最後，會完全忽略在 Unicode 字串中遇到的任何 null 字元。</p> | 
| <p>JET_coltypLongBinary<br />11</p> | <p>固定或可變長度的原始二進位資料行，長度最多可達2147483647個位元組。 此類型被視為 Long 值。 Long 值是特殊值，因為它可能很大，而且可以存取為數據流。 此類型也與 JET_coltypBinary 相同。</p> | 
| <p>JET_coltypLongText<br />12</p> | <p>固定或可變長度的文字資料行，長度最多可達2147483647個 ASCII 字元或1073741823個 Unicode 字元。 此類型被視為 Long 值。 Long 值是特殊值，因為它可能很大，而且可以存取為數據流。 此類型也與 JET_coltypText 相同。</p> | 
| <p>JET_coltypSLV<br />13</p> | <p>此資料行類型已淘汰。</p> | 
| <p>JET_coltypUnsignedLong<br />14</p> | <p>4位元組不帶正負號的整數，可採用 0 (零) 和4294967295之間的值。</p><p><strong>Windows Vista 和 Windows Server 2008：</strong> Windows Vista Windows Server 2008 及更新版本支援此資料行類型。</p> | 
| <p>JET_coltypLongLong<br />15</p> | <p>8位元組帶正負號的整數，可採用-9223372036854775808 和9223372036854775807之間的值。 負數值會在正值之前排序。</p><p><strong>Windows Vista 和 Windows Server 2008：</strong> Windows Vista Windows Server 2008 及更新版本支援此資料行類型。</p> | 
| <p>JET_coltypGUID<br />16</p> | <p>固定長度16位元組的二進位資料行，原生表示 GUID 資料類型。 GUID 資料行值的排序方式與在標準格式 (（例如 {4999b5c0-7657-42d9-bdc1-4b779784e013} ) ）中，這些值會以字串排序。</p><p><strong>Windows Vista 和 Windows Server 2008：</strong> Windows Vista Windows Server 2008 及更新版本支援此資料行類型。</p> | 
| <p>JET_coltypUnsignedShort<br />17</p> | <p>2位元組不帶正負號的整數，可採用0到65535之間的值。</p><p><strong>Windows Vista 和 Windows Server 2008：</strong> Windows Vista Windows Server 2008 及更新版本支援此資料行類型。</p> | 
| <p>JET_coltypMax<br />18</p> | <p>常數，描述最大 (，也就是引擎所支援的最大有效) 資料行類型之一。</p><p>此值應謹慎使用，因為它會隨著支援新的資料行類型而變更。 例如，它在 Windows 2000 的常值與 Windows XP 和更新版本上的值不同。</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetAddColumn](./jetaddcolumn-function.md)  
[JetCreateTableColumnIndex](./jetcreatetablecolumnindex-function.md)
