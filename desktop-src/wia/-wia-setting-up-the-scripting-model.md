---
description: 若要使用 Windows 映像取得 (WIA) 腳本模型，您必須在電腦上安裝並註冊檔案 Wiascr.dll。
ms.assetid: 94b08833-9fbd-46cf-b6a3-71713cc6ac30
title: 設定腳本模型開發環境
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: f6b70d52e937e93f26f95926c5ec2319611b2e8d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104191391"
---
# <a name="setting-up-the-scripting-model-development-environment"></a>設定腳本模型開發環境

若要使用 Windows 映像取得 (WIA) 腳本模型，您必須在電腦上安裝並註冊檔案 Wiascr.dll。

> [!Note]  
> 此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。 請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

將此檔案從 WIA SDK 複製到 *% windir%*/System32 (例如，c： \\ windows \\ System32) 目錄。 在命令列中，流覽至此目錄，然後輸入 **regsvr32 Wiascr.dll**。

這會在系統登錄中輸入必要的資訊。

您現在已準備好使用 WIA 腳本模型。

 

 
