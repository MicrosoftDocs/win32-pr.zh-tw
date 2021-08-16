---
description: CIM 架構相容性
ms.assetid: 3738914d-dd33-4999-b37f-b4bb94689cd4
ms.tgt_platform: multiple
title: CIM 架構相容性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5c3d87f1e40a52998f3a53a9b06f0572d8916b4a53663354ca5ffde67beaeed0
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118319784"
---
# <a name="cim-schema-compatibility"></a>CIM 架構相容性

Windows Management Instrumentation (WMI) 基礎結構的重要元件，是系統中可管理之實體的面向物件模型。 此模型符合桌面管理工作強制 ([DMTF](https://www.dmtf.org/standards/wsman)) 所維護的標準，也稱為通用訊息模型 (CIM) 。 CIM 架構會為其提供的任何資料提供單一資料描述機制。

從 Windows 7 開始，WMI 與 CIM 架構版本 2.17.1 ([https://www.dmtf.org/standards/cim/cim\_schema\_v2171/](https://www.dmtf.org/standards/cim/cim_schema_v2171)) 相容。 使用者現在可以在 Windows 電腦上編譯 DMTF 定義的架構。

## <a name="benefits-of-cim-schema-version-2171-compatibility"></a>CIM 架構版本2.17.1 相容性的優點

-   當使用者下載 CIM 架構版本2.17.1 或 DMTF MOF 檔案時，可以在目標 Windows 電腦上順利編譯。
-   CIM 架構版本2.17.1 新增了對 BIOS、印表機、標準訊息、作業系統狀態、新式電源管理範例、虛擬化和安全性的支援。
-   CIM 架構版本2.1.7.1 提供其他設定檔支援。 如需詳細資訊，請參閱 [跨命名空間關聯的遍歷](cross-namespace-association-traversal.md)

 

 



