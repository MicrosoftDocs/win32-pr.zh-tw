---
title: 適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的
description: 適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的
ms.assetid: 8A6B6194-5867-4B76-BD7B-152FD8A7DD77
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3777d4df386b071166fcfa17a60654c62e039d9137f73deaf2d85d54e2519e1e
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119028846"
---
# <a name="enhanced-storage-is-now-optional-for-winpe-and-server-sku"></a>適用于 WINPE 和伺服器 SKU 的增強式儲存體現在是選擇性的

## <a name="platforms"></a>平台

**用戶端**– Windows 8  
**伺服器**– Windows Server 2012  


## <a name="description"></a>描述

Windows 7 USB 裝置一律提供增強的儲存體。 在 Windows 8 版本中，它可供所有存放裝置使用。 在以用戶端為基礎的裝置中，預設會啟用此功能;在 [伺服器裝置] 中，它是選擇性的，必須透過 Windows 預先安裝環境 (WinPE) 布建。

## <a name="manifestation"></a>表現

如果未啟用增強型存放裝置，伺服器裝置將會失敗。

開機裝置必須透過已啟用的 WinPE 進行布建。

## <a name="solution"></a>解決方案

由於強化的儲存體是運行時間伺服器的選擇性選項，因此開發人員必須將其新增至 WinPE，才能布建和啟用這些磁片磁碟機。 如需詳細資訊，請參閱部署指南。

然後伺服器系統管理員必須明確設定其伺服器，以使用增強的儲存體。

 

 




