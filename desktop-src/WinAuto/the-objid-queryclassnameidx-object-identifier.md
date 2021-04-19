---
title: OBJID_QUERYCLASSNAMEIDX 物件識別碼
description: Microsoft Active Accessibility 使用 OBJID \_ QUERYCLASSNAMEIDX 物件識別碼搭配 WM \_ GETOBJECT 訊息，以判斷標準 Windows 控制項或通用控制項所屬的類別。
ms.assetid: 2167df6d-5df3-40b7-bebe-142f4bd98cd7
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2ba7d73a152380411ef0b230de8f0e3372a6718b
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "106968011"
---
# <a name="the-objid_queryclassnameidx-object-identifier"></a>OBJID \_ QUERYCLASSNAMEIDX 物件識別碼

Microsoft Active Accessibility 使用 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) 物件識別碼搭配 [**WM \_ GETOBJECT**](wm-getobject.md) 訊息，以判斷標準 Windows 控制項或通用控制項所屬的類別。 控制項會藉由傳回 Microsoft Active Accessibility 對應至控制項之類別名稱的值，來回應此訊息。 Microsoft Active Accessibility 使用這種資訊來提供標準 Windows 控制項和通用控制項的協助工具支援。

一般來說，只有標準的 Windows 控制項和通用控制項會回應 [**OBJID \_ QUERYCLASSNAMEIDX**](object-identifiers.md) 物件識別碼。 不過，如果自訂控制項包含與現有標準 Windows 控制項或通用控制項相同的所有功能，也可能會回應。 這可讓 Microsoft Active Accessibility 所提供的其中一個標準 proxy 物件支援自訂控制項。

如需詳細資訊，請參閱 [附錄 F： OBJID \_ QUERYCLASSNAMEIDX 的物件識別碼值](appendix-f--object-identifier-values-for-objid-queryclassnameidx.md)。

 

 




