---
description: 深入瞭解： JET_SNT
title: JET_SNT
TOCTitle: JET_SNT
ms:assetid: 74ac5142-8102-4dd3-8f2a-786a7a2ac78f
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269294(v=EXCHG.10)
ms:contentKeyID: 32765586
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
ms.openlocfilehash: 250ad992ec26b218bab21691f26c0938b6be6921
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122481384"
---
# <a name="jet_snt"></a>JET_SNT


_**適用于：** Windows |Windows伺服器_

## <a name="jet_snt"></a>JET_SNT

[JET_SNT]()的常數群組描述作業的進度點，這是在呼叫[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函數時所要求的資訊。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_sntBegin<br />5</p> | <p>作業的開頭</p> | 
| <p>JET_sntRequirements<br />7</p> | <p>不支援。</p><p><strong>Windows 2000 伺服器：</strong> 作業已啟動。 在此情況下，回呼函式的最後一個參數應該是指向 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的有效指標，指出要執行的單位總數。</p> | 
| <p>JET_sntProgress<br />0</p> | <p>完成的單位數和尚未完成的單位數。 這項資訊會在 <a href="gg269328(v=exchg.10).md">JET_SNPROG</a> 結構的成員中傳回。</p> | 
| <p>JET_sntComplete<br />6</p> | <p>作業完成。</p> | 
| <p>JET_sntFail<br />3</p> | <p>作業失敗。</p> | 
| <p>JET_sntRecoveryStep<br />8</p> | <p>操作的復原控制。</p><div class="alert">&gt; [!NOTE]&gt; <P>此值不適用於從 Windows 8 開始的 Windows 作業系統版本。</P></div> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNP](./jet-snp.md)  
[JET_SNPROG](./jet-snprog-structure.md)
