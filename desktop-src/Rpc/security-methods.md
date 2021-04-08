---
title: 安全性方法
description: Microsoft RPC 支援兩種不同的方法，可將安全性新增至您的分散式應用程式。
ms.assetid: 10dd8e71-668a-46bf-ab5d-e4b1e0e56a46
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 367c4d052301ac1100d84cf18dc63e1540ed34b0
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104021901"
---
# <a name="security-methods"></a>安全性方法

Microsoft RPC 支援兩種不同的方法，可將安全性新增至您的分散式應用程式。 第一個方法是使用安全性支援提供者介面 (SSPI) ，您可以使用 RPC 函數來存取此介面。 一般而言，最好是使用這個方法。 SSPI 提供最具彈性且與網路無關的驗證功能。

第二種方法是使用系統傳輸通訊協定內建的安全性功能。 傳輸層級安全性方法並非慣用的方法。 建議使用 SSPI，因為它適用于所有跨平臺的傳輸，並提供高層級的安全性，包括隱私權。

本節提供下列主題中 SSPI 和傳輸層級安全性的概述：

-   [安全性支援提供者介面 (SSPI)](security-support-provider-interface-sspi-.md)
-   [傳輸安全性](transport-security.md)

 

 




