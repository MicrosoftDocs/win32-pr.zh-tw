---
title: 控制點安全性考慮
description: 當您在建立控制點時，必須考慮下列安全性問題。
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0165ad0c8a721b10d5cc34c49947a98f2c15d1de
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "103932428"
---
# <a name="control-point-security-considerations"></a>控制點安全性考慮

當您在建立控制點時，必須考慮下列安全性問題。

-   所有控制點搜尋預設會以 TTL 1 傳送。 這表示只會探索相同子網內的裝置。 您可以在登錄中設定較高的 TTL。
-   裝置的裝置和服務描述只會在已傳送裝置公告的相同裝置上存在時才會下載。
-   如果裝置的控制項和訂用帳戶 Url 位於傳送裝置宣告的相同裝置上，則裝置只會傳送控制權和訂用帳戶要求。

 

 




