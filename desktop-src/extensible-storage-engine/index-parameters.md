---
description: 深入瞭解：索引參數
title: 索引參數
TOCTitle: Index Parameters
ms:assetid: df3dfbc7-71fb-4ae2-a94a-b00eaa1572ec
ms:mtpsurl: https://msdn.microsoft.com/library/Gg294119(v=EXCHG.10)
ms:contentKeyID: 32765733
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
ms.openlocfilehash: 2901887233ff8b25114334c97e6a731072a69ce1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "104027508"
---
# <a name="index-parameters"></a>索引參數


_**適用于：** Windows |Windows Server_

## <a name="index-parameters"></a>索引參數

本主題包含用於索引的參數。

*JET_paramIndexTupleIncrement*  
132  

此參數會指定在產生每個元組時，用來逐步執行來源資料行值的位移增量的預設值。 如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>1</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows Vista 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTupleStart*  
133  

此參數會指定來源資料行值中的位移的預設值，而產生元組產生。 如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>0</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>0 - 32767</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows Vista 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMax*  
111  

此參數會針對元組索引中的最大元組長度指定預設值。 如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 結構。

**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。 若為 Windows Vista，則不再支援此功能。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>10</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>  0、2-255</p>
<p><strong>Windows Vista：</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesLengthMin*  
110  

此參數會針對元組索引中的最小元組長度指定預設值。 如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 。

**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。 若為 Windows Vista，則不再支援此功能。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>3</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003： </strong>  0、2-255</p>
<p><strong>Windows Vista：</strong>  2-255</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramIndexTuplesToIndexMax*  
112  

此參數會指定要細分為元組索引之元組的來源字串最大長度的預設值。 如需詳細資訊，請參閱 [JET_TUPLELIMITS](./jet-tuplelimits-structure.md) 。

**Windows Vista：**  在 Windows Vista 之前，將此參數設定為零會將它設回其預設值。 若為 Windows Vista，則不再支援此功能。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>32767</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>整數</p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p><strong>Windows 2000、WINDOWS XP 及 Windows Server 2003：</strong>  0 –32767</p>
<p><strong>Windows Vista：</strong>  1-32767</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>Windows XP 和更新版本</p></td>
</tr>
</tbody>
</table>


*JET_paramUnicodeIndexDefault*  
72  

此參數會控制 Unicode 索引鍵資料行上任何索引所使用的預設 Unicode 參數。 這個參數的型別是 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) 的，實際上是使用儲存在 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 和 [JetSetSystemParameter](./jetsetsystemparameter-function.md)的整數參數中的緩衝區指標來傳遞。 緩衝區的大小必須等於 [JET_UNICODEINDEX](./jet-unicodeindex-structure.md) 的大小，且必須使用字串緩衝區大小參數傳遞至 [JetGetSystemParameter](./jetgetsystemparameter-function.md) 。 這顯然不一致，但這是此參數的行為。

此參數的預設值包含美國英文地區設定的 LCID，以及下列 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標： LCMAP_SORTKEY、NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。

**Windows 2000：**  LCID 中的 SORTID 會被忽略。 一律會使用 SORT_DEFAULT 的 SORTID。

**Windows 2000：** [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa) 旗標必須包含下列旗標： LCMAP_SORTKEY、NORM_IGNORECASE、NORM_IGNOREKANATYPE 和 NORM_IGNOREWIDTH。 此外， [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標可能包含下列旗標： NORM_IGNORENONSPACE。

**注意**  如果您的應用程式希望儲存 Unicode 資料，強烈建議您不要依賴索引的預設 Unicode 參數。 使用美式英文的表示是使用不變的地區設定，而且已知的預設 [LCMapStringW](/windows/win32/api/winnls/nf-winnls-lcmapstringa)旗標會嚴重干擾某些語言。 您應該一律使用 [JET_INDEXCREATE](./jet-indexcreate-structure.md)，將 Unicode 參數的設定指定為 JetCreateIndex2。

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>預設值：3</p></td>
<td><p>特殊</p></td>
</tr>
<tr class="even">
<td><p>輸入：</p></td>
<td><p>JET_UNICODEINDEX * (JET_UNICODEINDEX) </p></td>
</tr>
<tr class="odd">
<td><p>有效範圍：</p></td>
<td><p>特殊</p></td>
</tr>
<tr class="even">
<td><p>範圍：</p></td>
<td><p>執行個體</p></td>
</tr>
<tr class="odd">
<td><p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p></td>
<td><p>Yes</p></td>
</tr>
<tr class="even">
<td><p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>會影響實體版面配置：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響可靠性：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>影響效能：</p></td>
<td><p>No</p></td>
</tr>
<tr class="even">
<td><p>會影響資源：</p></td>
<td><p>No</p></td>
</tr>
<tr class="odd">
<td><p>可用性：</p></td>
<td><p>全部</p></td>
</tr>
</tbody>
</table>


### <a name="requirements"></a>規格需求

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><strong>用戶端</strong></p></td>
<td><p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p></td>
</tr>
<tr class="even">
<td><p><strong>伺服器</strong></p></td>
<td><p>需要 Windows Server 2008、Windows Server 2003 或 Windows 2000 Server。</p></td>
</tr>
<tr class="odd">
<td><p><strong>標頭</strong></p></td>
<td><p>宣告于 Esent. h 中。</p></td>
</tr>
</tbody>
</table>


### <a name="see-also"></a>另請參閱

[JET_INDEXCREATE](./jet-indexcreate-structure.md)  
[JET_TUPLELIMITS](./jet-tuplelimits-structure.md)  
[JET_UNICODEINDEX](./jet-unicodeindex-structure.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetGetSystemParameter](./jetgetsystemparameter-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetSystemParameter](./jetsetsystemparameter-function.md)
