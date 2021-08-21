---
description: 深入瞭解：回呼參數
title: 回呼參數
TOCTitle: Callback Parameters
ms:assetid: 7f3cdc13-ffbd-4e5a-b650-1c6388e784dc
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269310(v=EXCHG.10)
ms:contentKeyID: 32765600
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
ms.openlocfilehash: a7b904c090852ea3990ac78e37a7ca851e152968
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122465215"
---
# <a name="callback-parameters"></a>回呼參數


_**適用于：** Windows |Windows伺服器_

## <a name="callback-parameters"></a>回呼參數

本主題包含用於回呼的參數。

*JET_paramDisableCallbacks*  
65  

此參數會停用應用程式提供之函式的所有 database engine 回呼。 它的主要目的是要支援資料庫引擎公用程式，而不是要在應用程式中使用。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



*JET_paramEnablePersistedCallbacks*  
156  

此參數可讓您在資料庫中使用持續性回呼。 在 Windows Vista 之前的版本中，預設會啟用持續性回呼的使用。 應用程式現在必須使用這個參數，在執行時間明確地啟用持續性回呼。 如果未設定此參數，則任何需要回呼回呼的資料庫作業都會失敗，並 JET_errCallbackFailed。 此參數不會影響在執行時間使用下列機制指定的任何回呼： JET_paramRuntimeCallback、 [JetRegisterCallback](./jetregistercallback-function.md)或對 JET API 的明確回呼參數。 即使不允許使用這些持續性回呼，仍可能建立包含持續性回呼的架構元素。 當此參數設定為 false 時，它會覆寫 JET_paramDisableCallbacks。


| | | <p>預設值：3</p> | <p>否</p> | | <p>輸入：</p> | <p>Boolean</p> | | <p>有效範圍：</p> | <p>False, True</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsVista 和更新版本</p> | 



*JET_paramRuntimeCallback*  
73  

此參數會使用執行 [JET_CALLBACK](./jet-callback-callback-function.md) 介面的執行時間回呼函式來設定引擎。 基於下列原因，可能會呼叫這個回呼： [JET_cbtypFreeCursorLS](./jet-cbtyp.md)、 [JET_cbtypFreeTableLS](./jet-cbtyp.md)或 [JET_cbtypNull](./jet-cbtyp.md)。 如需詳細資訊，請參閱 [JetSetLS](./jetsetls-function.md) 。


| | | <p>預設值：3</p> | <p>NULL</p> | | <p>輸入：</p> | <p>函數指標 (JET_API_PTR) </p> | | <p>有效範圍：</p> | <p>Null、 <a href="gg294098(v=exchg.10).md">JET_CALLBACK</a>*</p> | | <p>範圍：</p> | <p>執行個體</p> | | <p>在 <a href="gg269354(v=exchg.10).md">JetCreateInstance</a>之後設定：</p> | <p>是</p> | | <p>在 <a href="gg294068(v=exchg.10).md">JetInit</a>之後設定：</p> | <p>否</p> | | <p>會影響實體版面配置：</p> | <p>否</p> | | <p>會影響可靠性：</p> | <p>否</p> | | <p>影響效能：</p> | <p>否</p> | | <p>會影響資源：</p> | <p>否</p> | | <p>可用性：</p> | <p>WindowsXP 和更新版本</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista 或 Windows XP。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008 或 Windows server 2003。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_API_PTR](./jet-api-ptr.md)  
[JET_CALLBACK](./jet-callback-callback-function.md)  
[JET_CBTYP](./jet-cbtyp.md)  
[JetCreateInstance](./jetcreateinstance-function.md)  
[JetInit](./jetinit-function.md)  
[JetSetLS](./jetsetls-function.md)
