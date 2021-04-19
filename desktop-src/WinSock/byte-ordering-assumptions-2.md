---
description: Winsock 中的 Sockaddr 結構和位元組順序假設。
ms.assetid: 792353eb-dc51-4c6d-b137-2d81083dc192
title: 位元組順序假設
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bfe6abf9ed46302bd037d1eb130b18c5568518cf
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106973272"
---
# <a name="byte-ordering-assumptions"></a>位元組順序假設

服務提供者應將所有 [**sockaddr**](sockaddr-2.md) 元件專有的位址系列參數視為在網路位元組順序中，並將位址家族參數視為本機電腦的位元組順序。 Winsock 應用程式必須負責確保 **sockaddr** 結構中所包含的位址已正確排列。 Winsock API 提供一些轉換常式，以簡化這項工作。 目前這些常式會瞭解本機主機的自然位元組順序以及位元組由大到小或位元組由大到小的網路位元組順序之間的轉換。 Winsock 架構未來可支援其他的位元組順序配置。

 

 



