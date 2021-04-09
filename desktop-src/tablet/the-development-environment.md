---
description: 您不需要 Tablet PC 來開發 Tablet PC 應用程式，但您需要能夠執行本主題稍後所列之軟體的個人電腦。
ms.assetid: 82034950-78a7-4bab-b449-1b8ea7d90676
title: 開發環境
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fefa29a518beaf21aa8b2457abf17d9581075f73
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "103945349"
---
# <a name="the-development-environment"></a>開發環境

您不需要 Tablet PC 來開發 Tablet PC 應用程式，但您需要能夠執行本主題稍後所列之軟體的個人電腦。

強烈建議您在實際的 Tablet PC 上測試您的應用程式，以確保系統會考慮硬體中的所有差異，例如較高的解析度數位板。

典型的最基本開發系統包含下列硬體和軟體。

## <a name="hardware"></a>硬體

-   8 MB 的硬碟空間以進行完整安裝。
-   輸入的指標裝置。 這包括像是滑鼠、外部平板電腦或具有隱藏的 Tablet PC 的裝置。

HID 代表人類介面裝置，這是輸入裝置的標準。 不符合 HID 規範的數位板被視為一般滑鼠，而符合 HID 規範的數位板在筆觸上具有較高的解析度和更多的中繼資料，例如壓力，類似于 Tablet PC 硬體上所安裝的壓力。

## <a name="software"></a>軟體

下列作業系統可以用來開發 Tablet PC 應用程式：

-   Windows 7
-   Windows Vista
-   Windows Server 2008
-   Windows XP Tablet PC Edition 2005
-   Windows Server 2003
-   Windows XP Professional

您也會需要：

-   Visual Studio 第6版（含 Service Pack 5）、Visual Studio .NET 或 Visual Studio .NET 2005
-   建議使用 Microsoft Internet Explorer 6 或更高版本 () 

### <a name="details-on-developing-on-non-tablet-pc-skus-of-windows"></a>在 Windows 的非 Tablet PC Sku 上進行開發的詳細資料

Tablet PC 平臺元件可以安裝在 Windows XP Professional Service Pack 2 或 Windows Server 2003 上。 在這些作業系統上，您的應用程式可以使用 [**InkCollector**](inkcollector-class.md) 類別來收集筆墨，並且可以進行測試和調試。 不過，除非您同時安裝 Microsoft Windows XP Tablet PC Edition 2005 辨識器套件，否則無法使用任何辨識。 您可以從 MSDN 上的下載中心下載該套件。

將 Windows SDK 安裝到 Windows XP Professional 或 Windows Server 2003 系統之後，您將擁有建立筆跡應用程式所需的所有開發檔案 (例如 COM 開發人員) 的 msinkaut。 不過，在您安裝執行時間檔案之前，您將無法在該系統上執行或錯用應用程式。 比方說，如果是 COM 開發人員，就必須安裝並註冊 inkobj.dll。 由於您不是在具有這些平臺檔案的系統上，因此您必須從可轉散發合併模組（mstpcrt）安裝 Tablet PC 平臺元件，才能取得系統上的執行時間檔案。

將安裝在 Windows XP Professional 或 Windows 2000 系統上的平臺執行時間用於開發的最簡單方式，就是編譯行動電腦和 Tablet PC 範例所提供的範例安裝程式專案，然後將它部署到開發電腦上。

> [!Note]  
> Windows Vista 和 Windows XP Tablet PC Edition 2005 已安裝平臺元件，因此不需要額外的步驟來執行和錯用 Tablet PC 應用程式。

 

[InkEdit](inkedit-control-reference.md)和[InkPicture](inkpicture-control-reference.md)控制項可以用來在 Windows 2000 （含 service Pack 4）或 Windows XP Professional service pack 2 上，透過安裝 tablet pc SDK 1.7 版來收集筆墨，但無法在未安裝 tablet pc 平臺元件的非 tablet pc 系統上收集筆跡。

Windows SDK 提供在 Windows 的非平板電腦 Sku 上開發 Tablet PC 應用程式所需的所有元件。 將下列 **DWORD** 登錄機碼設定為1，以便在 Windows 的非平板電腦 sku 上收集筆墨：

`HKEY_LOCAL_MACHINE\SOFTWARE\Microsoft\TabletPC\Controls\EnableInkCollectionOnNonTablets`

此金鑰僅供開發之用。

 

 



