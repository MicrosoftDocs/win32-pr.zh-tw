---
description: 藉由將 sa \_ netnum 和 sa \_ nodenum 欄位設定為二進位 (1) ，即可達到透過網際網路進行的一般廣播。
ms.assetid: a56f3059-d6e5-42eb-8ba2-16071fffafa5
title: 所有路由廣播
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d0a5f0ba1e900dd390610a3bd3af2f779d523ae4a08973596e7da6b8331acc31
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118322717"
---
# <a name="all-routes-broadcast"></a>所有路由廣播

藉由將 **sa \_ netnum** 和 **sa \_ nodenum** 欄位設定為二進位 (1) ，即可達到透過網際網路進行的一般廣播。 服務提供者會將此要求轉譯為類型20的封包，而這是由 IPX 路由器辨識和轉寄的封包。 封包會造訪所有子網，而且可能會重複數次。 接收者必須處理數個重複的資料包複本。

這種廣播類型是在網路系統管理員之間不，所以其使用應非常有限。 許多路由器會停用這種類型的廣播，讓封包的部分不會被隱藏。

 

 



