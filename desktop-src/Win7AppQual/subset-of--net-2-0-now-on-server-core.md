---
description: 現在是在 Server Core 上的 .NET 2.0 子集
ms.assetid: f91c4604-b2d6-41e5-be66-bbc8a4f0e28e
title: 現在是在 Server Core 上的 .NET 2.0 子集
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8a9da259186f0eaea7999df6dde6d42d972484c35eee24c9b9efb7fc6a5d882b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118994628"
---
# <a name="subset-of-net-20-now-on-server-core"></a>現在是在 Server Core 上的 .NET 2.0 子集

## <a name="platform"></a>平台

**伺服器**-Windows Server 2008 R2  



## <a name="feature-impact"></a>功能影響

 **嚴重性** -低  
**頻率** -低  





## <a name="description"></a>Description

Windows server 2008 R2 的 server Core 安裝選項現在包含 .NET Framework 2.0 的子集。 子集是 .NET 2.0 中與 Server Core 中的功能相符的功能;未將任何二進位檔新增至 Server Core 基底，以允許 .NET 2.0 的任何部分正常運作。

Windows server 2008 的 server Core 安裝選項中沒有 .net 支援。

## <a name="manifestation-of-impact"></a>影響的表現

這可讓某些以 .net 2.0 為基礎的應用程式在 Windows server 2008 R2 的 server Core 上執行。

## <a name="testing"></a>測試

確認您的程式碼所使用的 .NET 類別包含在 Server Core 中。 也請測試在 Server Core 上執行此程式碼的任何應用程式。

## <a name="links-to-other-resources"></a>其他資源的連結

-   [Server Core](/previous-versions/windows/desktop/legacy/ms723891(v=vs.85))
-   [Server Core Blog](https://blogs.technet.com/server_core/archive/2008/11/25/net-2-0-and-server-core-in-windows-server-2008-r2.aspx)
-   另 *請參閱* *Windows server 2008 R2 SDK* 的 server Core 區段（當它變成可用時）

> [!Note]  
> 這些資源可能無法在某些語言及國家/地區中使用。

 

 

 
