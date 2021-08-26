---
title: 金鑰取得函式
description: 根據預設，SSP 會提供加密金鑰給提出要求的伺服器程式。 每個 SSP 都會實行自己產生金鑰的系統。 SSP 產生的金鑰格式是 SSP 專屬的。
ms.assetid: 0ba7212c-6ee8-4a92-94d0-f09f84b05bf3
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 292926f53e5af0e75957f9b363d3917b1c5f68ef3a4e0a0acf7111c6b37b6518
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120020230"
---
# <a name="key-acquisition-functions"></a>金鑰取得函式

根據預設，SSP 會提供加密金鑰給提出要求的伺服器程式。 每個 SSP 都會實行自己產生金鑰的系統。 SSP 產生的金鑰格式是 SSP 專屬的。

RPC 能讓您覆寫產生加密金鑰的預設方法。 您的應用程式可以呼叫 [**RpcServerRegisterAuthInfo**](/windows/desktop/api/Rpcdce/nf-rpcdce-rpcserverregisterauthinfo) 函式，並將指標傳遞給金鑰取得函數。 您可以撰寫金鑰取得函式，讓它使用您所選擇的任何方法來產生金鑰。 不過，它傳遞給伺服器程式的金鑰必須符合 SSP 需要的格式。

> [!Note]  
> 大部分的應用程式都不需要使用金鑰取得函式，而且可以直接將 **Null** 提供給要求金鑰取得函式的所有參數。

 

 

 




