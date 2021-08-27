---
description: 深入瞭解：錯誤處理常數
title: 錯誤處理常數
TOCTitle: Error Handling Constants
ms:assetid: 5a1f9438-2d36-483e-9820-d0de30ee5e01
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269258(v=EXCHG.10)
ms:contentKeyID: 32765560
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
ms.openlocfilehash: 4480b54277c1586ca05d4a5db2ca6fdb9e045055
ms.sourcegitcommit: 4665ebce0c106bdb52eef36e544280b496b6f50b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/26/2021
ms.locfileid: "122987631"
---
# <a name="error-handling-constants"></a>錯誤處理常數


_**適用于：** Windows |Windows伺服器_

## <a name="error-handling-constants"></a>錯誤處理常數

下列常數可用來設定 [JET_paramExceptionAction](./error-handling-parameters.md) 系統參數的範圍。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_ExceptionMsgBox<br />0x0001</p> | <p>發生例外狀況時顯示訊息方塊。</p> | 
| <p>JET_ExceptionNone<br />0x0002</p> | <p>發生例外狀況時，不執行任何動作。</p> | 



### <a name="requirements"></a>規格需求


| 需求 | 值 |
|------------|----------|
| <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | 
| <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | 
| <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 



### <a name="see-also"></a>另請參閱

[錯誤處理參數](./error-handling-parameters.md)
