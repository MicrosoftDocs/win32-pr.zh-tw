---
description: 深入瞭解：資訊參數
title: 資訊參數
TOCTitle: Informational Parameters
ms:assetid: 48500fc9-6d89-45b8-92ad-afb997b729f3
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269241(v=EXCHG.10)
ms:contentKeyID: 32765543
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
ms.openlocfilehash: 62adda8c818124b905cf81a2114cddd6556c3d13
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122469525"
---
# <a name="informational-parameters"></a>資訊參數


_**適用于：** Windows |Windows伺服器_

## <a name="informational-parameters"></a>資訊參數

本主題包含用來公開資料庫引擎相關資訊的參數。

*JET_paramKeyMost*  
134  

這個唯讀參數表示可針對目前資料庫頁面大小選取的最大可允許索引鍵長度， (如 JET_paramDatabasePageSize) 所設定。


| | | <p>預設值：3</p> | <p>JET_cbKeyMost4KBytePage</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>255–65535</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>N/A</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>N/A</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>從 Windows Server 2008 和 Windows Vista 開始</p> | 



*JET_paramMaxColtyp*  
131  

這個唯讀參數會傳回該版本資料庫引擎的最大 [JET_COLTYP](./jet-coltyp.md) (JET_coltypMax) 。 這個值可以用來測試特定 [JET_COLTYP](./jet-coltyp.md)的支援。 如果給定的 [JET_COLTYP](./jet-coltyp.md) 小於這個參數的值，database engine 就會支援它。


| | | <p>預設值：3</p> | <p>JET_coltypUnsignedShort + 1</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-255</p> | | <p>範圍：</p> | <p>全球</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>N/A</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>N/A</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>從 Windows Server 2008 和 Windows Vista 開始</p> | 



*JET_paramLVChunkSizeMost*  
163  

唯讀參數，會根據設定的頁面大小傳回長值的區塊大小。 如果要使用多個 Jet {Set，抓取} 資料行呼叫來讀取或寫入較長的值，則使用大小是區塊大小倍數的緩衝區會更有效率。


| | | <p>預設值：3</p> | <p>2kb 頁面 = 1966 位元組<br />4 kb 頁面 = 4014 個位元組<br />8kb 頁面 = 8110 位元組<br />16kb 頁面 = 4050 位元組<br />32kb 頁面 = 8150 位元組</p> | | <p>輸入：</p> | <p>整數</p> | | <p>有效範圍：</p> | <p>0-10000</p> | | <p>範圍：</p> | <p></p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p></p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p></p> | | <p>會影響實體版面配置：</p> | <p></p> | | <p>會影響可靠性：</p> | <p></p> | | <p>影響效能：</p> | <p></p> | | <p>會影響資源：</p> | <p></p> | | <p>可用性：</p> | <p></p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows Server 2008。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JET_COLTYP](./jet-coltyp.md)
