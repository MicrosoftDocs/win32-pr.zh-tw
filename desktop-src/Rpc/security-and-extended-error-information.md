---
title: 安全性和延伸錯誤資訊
description: 擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。
ms.assetid: ca6ef213-e59d-4b4e-ae7e-f5b20d11fd01
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f246e86dee31ea5e755c45211e3bd949657cdf95c37bf6ab4de3706be09fdec3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118925685"
---
# <a name="security-and-extended-error-information"></a>安全性和延伸錯誤資訊

擴充的錯誤資訊會在疑難排解 RPC 問題時提供非常有用的資料，但這類資料很容易由安全性重視的組織視為機密。 考慮到這類安全性問題，預設會關閉擴充的錯誤資訊。

當停用擴充的錯誤資訊時，仍會產生擴充的錯誤資訊，但絕對不會在進程或電腦界限之間傳輸資訊。 這種方法可讓有權存取進程位址空間的工具（例如偵錯工具）使用錯誤資訊。 開啟時，會產生擴充的錯誤資訊，並且可以跨進程和電腦界限傳送這些資訊。 目前，擴充的錯誤資訊用於連接導向的通訊協定序列和本機 RPC (LRPC) 。 它會針對資料包部分實行。

 

 




