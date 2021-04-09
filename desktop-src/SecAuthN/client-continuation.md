---
description: 某些通訊協定需要多個驗證訊息。
ms.assetid: b4c4c38c-0286-49b1-b93d-4c6b885fe0f6
title: 用戶端接續
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: ca363489cf87a8fdf2743a8c26a7848c257212e1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848667"
---
# <a name="client-continuation"></a>用戶端接續

某些通訊協定需要多個驗證訊息。 在此情況下，用戶端會剖析伺服器的回應，並使用上一個呼叫的 [繼續] 狀態，再次呼叫 [**InitializeSecurityCoNtext (一般)**](/windows/win32/api/sspi/nf-sspi-initializesecuritycontexta) 。 用戶端會檢查此呼叫的傳回狀態，而且可能需要繼續進行額外的腿。 它會使用 *pOutput* 中的資訊來建立訊息，並將它傳送至伺服器。

 

 
