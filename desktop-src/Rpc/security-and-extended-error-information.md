---
title: 安全性和延伸錯誤資訊
description: 擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7b2029b40937dcef0622f6163e5e8f95b7006ade
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103675235"
---
# <a name="security-and-extended-error-information"></a>安全性和延伸錯誤資訊

擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。 考慮到這類安全性問題，預設會關閉擴充的錯誤資訊。

當停用擴充的錯誤資訊時，仍會產生擴充的錯誤資訊，但絕對不會在進程或電腦界限之間傳輸資訊。 這種方法可讓有權存取進程位址空間的工具（例如偵錯工具）使用錯誤資訊。 開啟時，會產生擴充的錯誤資訊，並且可以跨進程和電腦界限傳送這些資訊。 目前，擴充的錯誤資訊用於連接導向的通訊協定序列和本機 RPC (LRPC) 。 它會針對資料包部分實行。

 

 




