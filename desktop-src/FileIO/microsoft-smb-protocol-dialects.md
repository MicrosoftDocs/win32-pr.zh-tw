---
description: 若要使用 Microsoft SMB 通訊協定在用戶端與伺服器之間建立連線，您必須先使用用戶端和伺服器支援的最高層級功能來判斷方言。
ms.assetid: ad48391b-fcc7-4e58-83bb-6084503c8d61
title: Microsoft SMB 通訊協定方言
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f35d3fbcaa3345e2981df797f115e88064e38f04
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468952"
---
# <a name="microsoft-smb-protocol-dialects"></a>Microsoft SMB 通訊協定方言

Microsoft SMB 通訊協定訊息封包的清單已成長多年，以配合 Microsoft SMB 通訊協定的增強功能，而現在是數百個數字。 其成長的每個階段都是由標準的封包集或方言所標示。 每個方言都會以標準字串來識別，例如「電腦網路程式1.0」、「MICROSOFT 網路3.0」、「DOS LANMAN 2.1」或「NT LM 0.12」。 第一個字串會識別 SMB 的第一個方言，而最後一個字串會識別 CIFS，也就是 Microsoft SMB 通訊協定的第一個方言。

大部分的 Windows 用戶端至少都支援六種不同的 Microsoft SMB 通訊協定方言，因此在用戶端與使用 Microsoft SMB 通訊協定的伺服器之間建立連線的第一個步驟，是使用用戶端和伺服器支援的最高層級功能來判斷方言。 此流程稱為「正在協商方言」。 上述的方言字串包含在方言協商要求和回應封包中，以供此用途之用。

 

 



