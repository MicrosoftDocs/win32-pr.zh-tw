---
title: 定義介面
description: 介面定義是用戶端應用程式和伺服器應用程式彼此通訊方式的正式規格。
ms.assetid: 709ca498-4da3-4e6f-bb12-333a407b74c2
keywords:
- 遠端程序呼叫 RPC、作業、定義介面
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8c9f447847eeca39258b96ba129c46b3f7bcf054
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021131"
---
# <a name="defining-the-interface"></a>定義介面

介面定義是用戶端應用程式和伺服器應用程式彼此通訊方式的正式規格。 介面會定義用戶端和伺服器彼此辨識的方式、用戶端應用程式可以呼叫的遠端程式，以及這些程式的參數和傳回值的資料類型。 它也會指定如何在用戶端與伺服器之間傳輸資料。

您可以使用 Microsoft 介面定義語言 (MIDL) 來定義此介面，其中包含以關鍵字增強的 C 語言定義，稱為屬性，其描述如何透過網路傳輸資料。

 (IDL) 檔案的介面定義包含型別定義、屬性和函式原型，描述如何在網路上傳輸資料。 應用程式設定 (ACF) 檔所包含的屬性，可針對特定的作業環境設定您的應用程式，而不會影響其網路特性。

 

 




