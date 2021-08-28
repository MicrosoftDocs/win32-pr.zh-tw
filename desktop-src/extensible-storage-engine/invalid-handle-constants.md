---
description: 深入瞭解：不正確控制碼常數
title: 不正確控制碼常數
TOCTitle: Invalid Handle Constants
ms:assetid: 594d7804-725f-4f72-b5f0-56f099c1c17b
ms:mtpsurl: https://msdn.microsoft.com/library/Gg269256(v=EXCHG.10)
ms:contentKeyID: 32765558
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
ms.openlocfilehash: 28a52b2fc7a51572cc7bb78ad7631df41438310a
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122473274"
---
# <a name="invalid-handle-constants"></a>不正確控制碼常數


_**適用于：** Windows |Windows伺服器_

## <a name="invalid-handle-constants"></a>不正確控制碼常數

下列常數表示 ESE 不同方面的無效控制碼。


| <p>常數/值</p> | <p>Description</p> | 
|-----------------------|--------------------|
| <p>JET_instanceNil<br /> (~ (JET_INSTANCE) 0) </p> | <p>資料庫實例的控制碼無效。<br /><strong>Windows XP：</strong>Windows XP 引進。</p> | 
| <p>JET_sesidNil<br /> (~ (JET_SESID) 0) </p> | <p>會話識別碼的控制碼無效。</p> | 
| <p>JET_tableidNil<br /> (~ (JET_TABLEID) 0) </p> | <p>資料表識別碼的無效控制碼。</p> | 
| <p>JET_bitNil<br /> ( (JET_GRBIT) 0) </p> | <p>位群組的無效控制碼。</p> | 
| <p>JET_LSNil<br /> (~ (JET_LS) 0) </p> | <p>本機儲存體的無效控制碼。</p> | 
| <p>JET_dbidNil<br /> ( (JET_DBID) 0xFFFFFFFF) </p> | <p>資料庫識別碼的控制碼無效。</p> | 



### <a name="requirements"></a>規格需求


| | | <p><strong>用戶端</strong></p> | <p>需要 Windows Vista、Windows XP 或 Windows 2000 Professional。</p> | | <p><strong>伺服器</strong></p> | <p>需要 Windows server 2008、Windows Server 2003 或 Windows 2000 Server。</p> | | <p><strong>標頭</strong></p> | <p>宣告于 Esent. h 中。</p> | 


