---
title: " (RPC) 的授權函數"
description: 每次伺服器程式收到用戶端要求以存取其中一個管理遠端程式時，RPC 執行時間程式庫會叫用預設授權函數。
ms.assetid: e3edbf6f-2876-49ac-a93e-14fd0b5adf53
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 490c06ba8e40f132c17986edaef4dc02bbe056d7
ms.sourcegitcommit: 40a1246849dba8ececf54c716b2794b99c96ad50
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/12/2019
ms.locfileid: "104022782"
---
# <a name="authorization-functions"></a>授權函數

每次伺服器程式收到用戶端要求以存取其中一個管理遠端程式時，RPC 執行時間程式庫會叫用預設授權函數。 此函數會使用 SSP 來檢查用戶端的認證，並授權或拒絕要求。

您的伺服器程式可以覆寫 SSP 提供的授權函數。 叫用函式 [**RpcMgmtSetAuthorizationFn**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtsetauthorizationfn) ，並將它傳遞至您的授權函數的位址。 一旦伺服器程式設定授權函數之後，RPC 執行時間程式庫會在每次伺服器程式收到其中一個管理功能的用戶端要求時呼叫它。 如需詳細資訊，請參閱 [**RpcMgmtIsServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtisserverlistening)、 [**RpcMgmtStopServerListening**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtstopserverlistening)、 [**RpcMgmtInqIfIds**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqifids)、 [**RpcMgmtInqServerPrincName**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqserverprincname)和 [**RpcMgmtInqStats**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcmgmtinqstats)。

 

 




