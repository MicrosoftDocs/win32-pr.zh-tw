---
description: 深入瞭解： JET_SNP
title: JET_SNP
TOCTitle: JET_SNP
ms:assetid: 7f3d1cc5-7b27-454d-8dd1-584ab4b60ab0
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269311(v=EXCHG.10)
ms:contentKeyID: 32765601
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
ms.openlocfilehash: ee83dc86aa6faf5fab0b45596a586c657e4c6e2a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122474124"
---
# <a name="jet_snp"></a>JET_SNP


_**適用于：** Windows |Windows伺服器_

## <a name="jet_snp"></a>JET_SNP

**JET_SNP** 的常數群組描述要取得進度資訊的作業類型。 這些常數會當做 [JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)回呼函數的 *.snp* 參數使用。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_snpRepair<br />2</p> | <p>回呼是用於修復作業。</p> | 
| <p>JET_snpCompact<br />4</p> | <p>回呼適用于資料庫磁碟重組。</p> | 
| <p>JET_snpRestore<br />8</p> | <p>回呼是用於還原作業。</p> | 
| <p>JET_snpBackup<br />9</p> | <p>回呼適用于備份作業。</p> | 
| <p>JET_snpUpgrade<br />10</p> | <p>不支援。</p><p><strong>Windows 2000：</strong> 回呼適用于資料庫格式升級作業。</p> | 
| <p>JET_snpScrub<br />11</p> | <p>回呼適用于資料庫清空 (也就是清除) 作業。</p><p><strong>Windows server 2003 和 Windows 2000 伺服器：</strong> 不支援。</p> | 
| <p>JET_snpUpgradeRecordFormat<br />12</p> | <p>回呼是用於升級所有資料庫頁面之記錄格式的程式。</p><p><strong>Windows server 2003 和 Windows 2000 伺服器：</strong> 不支援。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[JET_PFNSTATUS](./jet-pfnstatus-callback-function.md)  
[JET_SNPROG](./jet-snprog-structure.md)  
[JET_SNT](./jet-snt.md)
