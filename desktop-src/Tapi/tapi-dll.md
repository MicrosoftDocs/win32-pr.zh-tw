---
description: TAPI Dll 以及 TAPI 伺服器 (Tapisvr.exe) ，都是將終端使用者或伺服器應用程式與服務提供者分隔的重要抽象概念。 與 TAPI 伺服器搭配的 TAPI DLL 在這兩層之間提供一致的介面。
ms.assetid: 17937bf1-e0bd-4845-9484-d23190807642
title: TAPI DLL
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 4ff26274baf25047212a3f9f8e15c2211d90cbaa10db23674ae54dbb97bbfdf7
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120012200"
---
# <a name="tapi-dll"></a>TAPI DLL

TAPI Dll 以及 TAPI 伺服器 (Tapisvr.exe) ，都是將終端使用者或伺服器應用程式與服務提供者分隔的重要抽象概念。 與 TAPI 伺服器搭配的 TAPI DLL 在這兩層之間提供一致的介面。

TAPI 應用程式會將適當的 DLL 載入其進程空間。 在初始化期間，TAPI 會建立與 Tapisvr.exe 的 RPC 連結。 TAPI 伺服器是在 SVCHOST 的內容中執行。

有三個與 TAPI 相關聯的 Dll： Tapi.dll、Tapi32.dll 和 Tapi3.dll。 這些 Dll 位於% SystemRoot% system32 中 \\ 。 下圖說明在 Microsoft 電話語音中各自角色的角色：

![三個 tapi dll 的角色](images/dllserv.png)

現有的16位應用程式連結至 Tapi.dll。 Tapi.dll 只是一個 Thunk 層，可將16位位址對應到32位位址，並將要求傳遞給 Tapi32.dll。

現有的32位 TAPI 2.x 應用程式會連結至 Tapi32.dll。 Tapi32.dll 是一種精簡的封送處理層，可將函式要求傳輸至 TAPI 伺服器 (TAPISRV) 並且在需要時，在應用程式的進程中載入及叫用媒體服務提供者 Dll。

TAPI 2.x 應用程式會連結至 Tapi3.dll。

 

 



