---
description: '[轉換] 屬性包含安裝套件的轉換清單。 安裝程式會在每次安裝、公告、隨選安裝或封裝的維護安裝時，套用轉換清單中的所有轉換。'
ms.assetid: dde2ef55-7794-4eb1-984a-ed13e990c97f
title: 套用轉換
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 2367e02396ec33e517f8abfe579060c0a0986be2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "103848970"
---
# <a name="applying-transforms"></a>套用轉換

[ [**轉換**](transforms.md) ] 屬性包含安裝套件的轉換清單。 安裝程式會在每次安裝、公告、隨選安裝或封裝的維護安裝時，套用轉換清單中的所有轉換。

[**轉換**](transforms.md)屬性是藉由在命令列上指定轉換的清單來設定。不過，使用/jm 或/ju [命令列選項](command-line-options.md)時，必須使用/t 選項指定轉換清單。

請注意，無法在安裝後修改轉換清單，而且只能藉由卸載應用程式來移除。

> [!Note]  
> 在安裝應用程式或更新時，Windows Installer 套件可以套用255以上的轉換。 當需要許多轉換時，應該將它們合併，且應該消除先前已淘汰的轉換。

 

下表提供各種可新增至轉換清單的轉換字串範例。



| 轉換字串                                                                                                              | Description                                                                                                                                                                                                                                                                                                                                                                             |
|--------------------------------------------------------------------------------------------------------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| transform1 .mst;： transform2 .mst;： transform3 .mst                                                                                 | Transform2 .mst 和 transform3 是 [內嵌的轉換](embedded-transforms.md)。 transform1 只有在已設定 [**TRANSFORMSSECURE**](transformssecure.md)屬性或 [TRANSFORMSSECURE 原則](transformssecure-policy.md)時，才是 [安全的來源轉換](secure-at-source-transforms.md)，否則 transform1 是不 [安全的轉換](unsecured-transforms.md)。 |
| \\\\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst;： transform2 .mst                                                                        | Transform2 是 [內嵌的轉換](embedded-transforms.md)。 transform1 只有在設定 [**TRANSFORMSSECURE**](transformssecure.md)屬性或 [TRANSFORMSSECURE 原則](transformssecure-policy.md)時，才會使用 [安全的完整路徑轉換](secure-full-path-transforms.md)，否則 transform1 是不安全的 [轉換](unsecured-transforms.md)。                   |
| @： transform2 .mst; transform1 .mst @transform1.mst ;： transform2 .mst<br/>                                                     | Transform2 是內嵌的轉換。 transform1 是獨立的 [安全來源轉換](secure-at-source-transforms.md)。                                                                                                                                                                                                                                                |
| \|\\\\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst;： transform2 .mst \| ： transform2 .mst; \\ \\伺服器 \\ 共用 \\ 路徑 \\ transform1 .mst<br/> | Transform2 是內嵌的轉換。 transform1 是獨立的 [安全-完整路徑轉換](secure-full-path-transforms.md)。                                                                                                                                                                                                                                                 |



 

 

 




