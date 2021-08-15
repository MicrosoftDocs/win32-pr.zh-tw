---
title: Windows Deployment Services
description: 部署 Windows 作業系統。 使用以網路為基礎的安裝來設定新的用戶端，而不需要系統管理員造訪每部電腦或直接從 CD 或 DVD 媒體安裝。
ms.assetid: 790abc27-03cc-4f93-bf04-a4eb37e614bb
keywords:
- Windows部署服務 Windows 部署服務
- Windows部署服務 Windows 部署服務，首頁
- 部署服務 Windows 部署服務
- WDS Windows 部署服務查看 Windows 部署服務
- 遠端安裝服務 Windows 部署服務查看 Windows 部署服務
- RIS Windows 部署服務查看 Windows 部署服務
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 100483541420015ed84a95543f2f94bafb2d509d44e6b321b53729caa94588cc
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119999508"
---
# <a name="windows-deployment-services"></a>Windows Deployment Services

## <a name="purpose"></a>目的

Windows部署服務 (WDS) 是 (RIS) 之遠端安裝服務的修訂版本。 WDS 可讓您部署 Windows 作業系統。 您可以使用 WDS 以網路為基礎的安裝來設定新的用戶端，而不需要系統管理員造訪每部電腦或直接從 CD 或 DVD 媒體安裝。

## <a name="developer-audience"></a>開發人員對象

WDS API 的主要開發人員物件是針對為 IT 和其他電腦管理群組開發自訂工具和進程的群組。 在無法使用標準 Windows 部署服務 (wds) 解決方案的環境中，wds API 可讓您以程式設計方式存取某些 WDS 元件。

原始設備製造商 (oem) 、系統建造商和企業 IT 專業人員尋找如何在新電腦上部署 Windows 的相關資訊，請參閱《 [ (更新逐步指南》](/previous-versions/windows/it-pro/windows-vista/cc766320(v=ws.10))中的標準 Windows 部署服務) WDS Windows 部署服務解決方案的相關資訊，以及 Windows 的[自動安裝套件 (WAIK) ](https://www.microsoft.com/download/details.aspx?id=10333)。

## <a name="run-time-requirements"></a>執行階段需求求

WDS 可作為 Windows server 2003 service pack 1 (SP1) 的附加元件使用，並包含在作業系統中，從 Windows Server 2003 service pack 2 (SP2) 和 Windows Server 2008 開始。 WDS PXE 伺服器 API 需要伺服器上的 WDS 伺服器角色，才能執行自訂 PXE 提供者。 WDS 用戶端 API 需要 Microsoft Windows 預先安裝環境 (Windows PE 2.0) 安裝程式處理階段。 中 Windows PE 2.0 的 RAMDISK 可開機映射。必須在網路開機程式中下載 WIM 格式，才能執行自訂 WDS 用戶端。

## <a name="in-this-section"></a>本節內容



| 主題                                                                                                 | 描述                                                                    |
|-------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
| [關於 Windows 部署服務 API](about-the-windows-deployment-services-api.md)<br/> | WDS 伺服器 API 和 WDS 用戶端 API 的一般資訊。<br/>    |
| [Windows部署服務參考](windows-deployment-services-reference.md)<br/>         | 描述 Windows 部署服務函數和結構。<br/> |



 

 

