---
description: DuplicateHandle 函式會建立一個重複的控制碼，以供另一個指定的進程使用。
ms.assetid: b79d2b8f-931e-4cab-9bbe-9ead1b102132
title: 物件重複
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0927f9d3b60f358623e66a067e75992e71c76ca5fe072a9749c9bbc217bfa2ec
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118886338"
---
# <a name="object-duplication"></a>物件重複

[**DuplicateHandle**](/windows/win32/api/handleapi/nf-handleapi-duplicatehandle)函式會建立一個重複的控制碼，以供另一個指定的進程使用。 這個共用物件控制碼的方法比使用命名物件或繼承更為複雜。 它需要建立進程和控制碼重複的進程之間的通訊。  (控制碼值和處理序識別碼) 所需的資訊，可由任何進程間的通訊方法（例如具名管道或命名的共用記憶體）進行通訊。

 

 
