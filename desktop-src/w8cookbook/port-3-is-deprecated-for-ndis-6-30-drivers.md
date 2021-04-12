---
title: NDIS 6.30 驅動程式的埠3已淘汰
description: NDIS 6.30 驅動程式的埠3已淘汰
ms.assetid: 900BD08D-3EAF-43F3-A74A-359815474FAD
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: df0b4c7f6a33b179a14d3d7f8151d3850e16dd44
ms.sourcegitcommit: ea4baf9953a78d2d6bd530b680601e39f3884541
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/01/2020
ms.locfileid: "104463833"
---
# <a name="port-3-is-deprecated-for-ndis-630-drivers"></a>NDIS 6.30 驅動程式的埠3已淘汰

## <a name="platforms"></a>平台

**用戶端** – Windows 8  
**伺服器** – Windows Server 2012  


## <a name="description"></a>Description

Windows 8 移除適用于 NDIS 微型埠 WLAN 驅動程式的平臺支援，以建立或啟動 IHV 擴充性埠 (也稱為第三個埠) 。 這項功能是在 Windows 7 中引進作為暫時量值，而 Wi-Fi 聯盟 (WFA) 開發 Wi-Fi 直接規格。 規格現在已完成，使用 Wi-Fi Direct 的產品已通過認證，Windows 8 引進原生 Wi-Fi 直接堆疊。

## <a name="manifestation"></a>表現

沒有，因為第三個埠是 WLAN 微型埠驅動程式需要這項功能時，會啟動的平臺功能。

## <a name="solution"></a>解決方法

我們會將擴充性埠功能保留給未回報 NDIS 6.30 的現有驅動程式，以維持裝置相容性。 不過，報告 NDIS 6.30 的新 WLAN 驅動程式將無法啟動此埠;相反地，這些驅動程式的開發人員應該使用 Wi-Fi Direct。

 

 




