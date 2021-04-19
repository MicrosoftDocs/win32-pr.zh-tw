---
description: 深入瞭解：導覽專案物件的樹狀結構
ms.assetid: e91f72c8-3ad6-49e8-88cc-aa99c13cd4c2
title: 流覽專案物件的樹狀結構
ms.topic: article
ms.date: 05/31/2018
topic_type:
- kbArticle
api_name: ''
api_type: ''
api_location: ''
ms.openlocfilehash: 04e87444c2b9c473268c5e97dd9c26d04d95b93b
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106971011"
---
# <a name="navigating-a-tree-of-item-objects"></a>流覽專案物件的樹狀結構

> [!Note]  
> 此腳本系統已取代為 Windows 映像取得 (WIA) Automation 層。 請參閱 [Windows 映像取得自動化層](/previous-versions/windows/desktop/wiaaut/-wiaaut-startpage)。

 

應用程式或腳本會流覽 Windows 映像取得 (WIA) 裝置的專案樹狀結構，以尋找並選取該裝置上的影像。 應用程式會使用這項技術，在不使用對話方塊的情況下，選取並取得影像。

WIA 裝置會以 [**專案**](-wia-item.md) 物件樹狀結構中的根專案表示。 樹狀結構中的子專案代表掃描器的資料夾和影像，或是掃描器的掃描張床。

連線到裝置之後，請在樹狀結構的根項目 (呼叫代表裝置的 [**專案**](-wia-item.md)物件的 [**子**](-wia-iwiadispatchitem-children.md)屬性，) 取得子專案的集合 (影像或掃描裝置的張床) 。

如果需要) 流覽專案樹狀結構，請以遞迴方式列舉此集合 (。

 

 
