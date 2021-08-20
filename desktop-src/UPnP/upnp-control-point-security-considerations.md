---
title: 控制點安全性考慮
description: 當您在建立控制點時，必須考慮下列安全性問題。
ms.assetid: 3281b4c3-d730-4273-9031-840a6ac655ce
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 85378d7f530177bb42a6751a13f643bad984e994ae65178c0ab06cd5ce4792a3
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118126005"
---
# <a name="control-point-security-considerations"></a>控制點安全性考慮

當您在建立控制點時，必須考慮下列安全性問題。

-   所有控制點搜尋預設會以 TTL 1 傳送。 這表示只會探索相同子網內的裝置。 您可以在登錄中設定較高的 TTL。
-   裝置的裝置和服務描述只會在已傳送裝置公告的相同裝置上存在時才會下載。
-   如果裝置的控制項和訂用帳戶 Url 位於傳送裝置宣告的相同裝置上，則裝置只會傳送控制權和訂用帳戶要求。

 

 




