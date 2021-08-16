---
title: 卸載具有未完成內容控制碼的伺服器
description: 傳統上，在不先停止裝載進程的情況下，卸載服務 RPC 呼叫的 DLL 是有問題的。
ms.assetid: d3880578-e542-418c-803a-fd00d0bfde7f
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: e581ff142c7453f4a9e9f1e40a5ab9991257a350a84b2fcb2ea08a0e157288cd
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119010946"
---
# <a name="unloading-a-server-with-outstanding-context-handles"></a>卸載具有未完成內容控制碼的伺服器

傳統上，在不先停止裝載進程的情況下，卸載服務 RPC 呼叫的 DLL 是有問題的。 這是因為卸載 DLL 時，執行關閉常式已不再有效。 當具有先前開啟之內容控制碼的用戶端失敗，而且 RPC 執行時間嘗試關閉內容控制碼時，嘗試呼叫向下執行常式存取會違反，而伺服器會當機。

從 Windows XP 開始，已新增名為 [**RpcServerUnregisterIfEx**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterifex)的新 API。 **RpcServerUnregisterIfEx** 會關閉正在取消註冊之介面開啟的內容控制碼; [**RpcServerUnregisterIf**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverunregisterif) 函數不會。 當整個進程關機時，並不需要使用 RpcServerUnregisterIfEx，但是如果有一個或多個裝載執行時間常式的 Dll 在未處理的內容控制碼存在時卸載，則需要使用 。

 

 




