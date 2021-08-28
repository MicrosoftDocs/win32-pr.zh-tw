---
description: Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。
ms.assetid: d7924e93-75e4-4f94-b159-02408535170d
title: 管理 DDE 共用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fa89b890c9cf2b140f669b5e4dfa556cd11f978d
ms.sourcegitcommit: 9b5faa61c38b2d0c432b7f2dbee8c127b0e28a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/19/2021
ms.locfileid: "122472164"
---
# <a name="managing-dde-shares"></a>管理 DDE 共用

\[不再支援網路 DDE。 Nddeapi.dll 存在於 Windows Vista 中，但所有的函式呼叫會傳回 NDDE \_ 未 \_ 執行。\]

Network DDE 提供可讓您刪除共用、取得或設定共用資訊，或列舉共用的函式。




| 工作 | 程序 | 
|------|-----------|
| 刪除 DDE 共用 | 使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a> 函數。 | 
| 取得 DDE 共用資訊 | 使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a> 函數。 | 
| 設定 DDE 共用資訊 | 使用 <a href="nddesharesetinfo.md"><strong>NDdeShareSetInfo</strong></a> 函數。 | 
| 列舉 DDE 共用 | 使用 <a href="nddeshareenum.md"><strong>NDdeShareEnum</strong></a> 函數。 您也可以使用 <a href="nddetrustedshareenum.md"><strong>NDdeTrustedShareEnum</strong></a> 函數來列舉受信任的 DDE 共用。<br /> | 
| 列舉已連線的使用者 | 使用 <a href="/windows/desktop/api/lmshare/nf-lmshare-netsessionenum"><strong>NetSessionEnum</strong></a> 函數。 | 
| 變更 DDE 共用名稱 | 刪除舊的共用並建立新的共用。<ol><li>使用 <a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>取出共用資訊。</li><li>使用 <a href="nddesharedel.md"><strong>NDdeShareDel</strong></a>移除共用。</li><li>變更<a href="nddesharegetinfo.md"><strong>NDdeShareGetInfo</strong></a>所傳回之<a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a>結構的<strong>lpszShareName</strong>成員。</li><li>將修改過的 <a href="nddeshareinfo-str.md"><strong>NDDESHAREINFO</strong></a> 結構傳遞至 <a href="nddeshareadd.md"><strong>NDdeShareAdd</strong></a>。</li></ol> | 




 

 

