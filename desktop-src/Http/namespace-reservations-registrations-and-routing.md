---
title: 命名空間保留、註冊和路由
description: 保留和註冊是 HTTP 伺服器 API 在電腦上提供 URL 命名空間存取權的作業。
ms.assetid: dc66960b-36cd-4c09-be0a-3aec9a8a25d8
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: a00801629b5b778bb6c87a0bff615cb9d5618f57
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104311091"
---
# <a name="namespace-reservations-registrations-and-routing"></a>命名空間保留、註冊和路由

保留和註冊是 HTTP 伺服器 API 在電腦上提供 URL 命名空間存取權的作業。 應用程式可以註冊一部分的 URL 命名空間，以便從 HTTP 用戶端服務要求。 應用程式會使用 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl) 函式，向 HTTP 伺服器 API 註冊命名空間。 HTTP 伺服器 API 會將 Url 新增至應用程式的要求佇列，並根據其佇列中的 Url 將要求路由傳送至應用程式。 不過，在應用程式可以註冊以接收 URL 命名空間的要求之前，系統管理員必須代表執行應用程式的使用者建立該 URL 的保留。 根據預設，命名空間是關閉的，也就是說，只有系統管理員可以註冊 >urlprefixes，直到系統管理員輸入保留為止。

保留會持續將 URL 命名空間的一部分配置給個別使用者，讓他們可以保留或「擁有」該部分的命名空間。 保留會授與使用者註冊命名空間服務要求的許可權。 HTTP 伺服器 API 可確保使用者不會從未擁有的命名空間部分註冊 Url。 為了確保命名空間安全性，Acl (存取控制清單) 會套用至為每個使用者保留的命名空間部分。

保留的命名空間是由 URL 前置詞字串所識別，以與用於註冊的 URL 前置詞相同的方式進行格式化。 這表示所有不同的主機規範類別也都可供保留。

命名空間保留會在重新開機時持續保存，而變更會動態生效，因此不需要停止並重新啟動電腦。

下列概念會在套用至註冊和保留命名空間的程式時進一步闡明。

-   註冊。 註冊是指應用程式用來表示接收指定 UrlPrefix 之要求的相關作業。 URL 註冊的 API 是 [**HttpAddUrl**](/windows/desktop/api/Http/nf-http-httpaddurl)。 註冊通常會在應用程式啟動期間發生，而且必須在每次應用程式啟動時執行。
-   路由。 路由是由 HTTP 伺服器 API 執行，以根據已註冊及/或保留的最符合 [UrlPrefix](urlprefix-strings.md) ，判斷要將要求分派至的應用程式。 路由作業會使用註冊和保留資訊。
-   預訂。 保留會將 URL 命名空間的一部分配置給一或多個使用者。 這種作業可讓使用者向右註冊指定的命名空間。 保留命名空間的使用者稱為 URL 命名空間的一部分。 命名空間保留通常是在安裝應用程式期間執行，而且是不頻繁的作業。 保留會在電腦重新開機時持續保存，而且需要具有電腦的系統管理員許可權或具有委派許可權的擁有權，才能建立或刪除。
-   代表團。 委派許可權可讓擁有命名空間的使用者將子樹的擁有權交給另一個使用者，使其成為後續的保留。 系統管理員會在進行保留時，將委派許可權授與使用者。 一個或多個使用者可以指派給命名空間的委派許可權。

 

 




