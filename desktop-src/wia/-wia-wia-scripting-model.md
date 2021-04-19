---
description: Windows 映像取得 (WIA) 提供自動化物件，以用於指令碼語言，例如 Microsoft JScript 和 Microsoft Visual Basic Scripting Edition (VBScript) 開發軟體，以及高階程式設計語言，例如 Microsoft Visual Basic 開發系統。
ms.assetid: 3d294db3-3349-4b26-aae1-1e3f588a0f0e
title: WIA 腳本模型
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: e70863e60e0d7aa6172bd9c93240f38cac27c6be
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971006"
---
# <a name="wia-scripting-model"></a>WIA 腳本模型

Windows 映像取得 (WIA) 提供自動化物件，以用於指令碼語言，例如 Microsoft JScript 和 Microsoft Visual Basic Scripting Edition (VBScript) 開發軟體，以及高階程式設計語言，例如 Microsoft Visual Basic 開發系統。

> [!Note]  
> 此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。 請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

下表說明 WIA 腳本物件和其使用方式。 

| Object                                | 描述                                                                                                                                                                                  |
|---------------------------------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| [**Wia**](-wia-wia.md)               | 最上層的 WIA 腳本物件。 使用 [**Wia**](-wia-wia.md) 物件來列舉和連接至裝置，以及處理硬體裝置事件。                                        |
| [**DeviceInfo**](-wia-deviceinfo.md) | [**DeviceInfo**](-wia-deviceinfo.md)物件可讓您存取裝置屬性的相關資訊。                                                                                     |
| [**項目**](-wia-item.md)             | 此物件代表 WIA 裝置、檔案和資料夾專案。 WIA 硬體裝置及其影像或掃描張床會以 [**專案**](-wia-item.md) 物件的階層式樹狀結構來表示。 |



 

[**DeviceInfo**](-wia-deviceinfo.md)物件和 [**Item**](-wia-item.md)物件都與集合物件相關聯。 如需使用集合物件的詳細資訊，請參閱使用 WIA 集合物件。

下列主題涵蓋使用 WIA 腳本模型的一般資訊：

-   [語法慣例](-wia-syntax-conventions.md)
-   [使用 WIA 集合物件](-wia-using-wia-collection-objects.md)
-   [WIA 屬性常數定義](-wia-wia-property-constant-definitions.md)

 

 
