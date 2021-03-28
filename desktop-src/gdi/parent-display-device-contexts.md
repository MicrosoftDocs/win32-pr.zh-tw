---
description: 父裝置內容可讓應用程式將設定視窗裁剪區域所需的時間減至最少。
ms.assetid: 194d5add-d1a1-4c10-89ee-171ff008a7ab
title: 父代顯示裝置內容
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0e423ceaa65790df35fa55c8dda597cb1bb45019
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104972593"
---
# <a name="parent-display-device-contexts"></a>父代顯示裝置內容

*父裝置內容* 可讓應用程式將設定視窗裁剪區域所需的時間減至最少。 應用程式通常會使用上層裝置內容來加速控制視窗的繪製，而不需要私人或類別的裝置內容。 例如，系統會使用推播按鈕和編輯控制項的父裝置內容。 父裝置內容僅適用于子視窗，絕不會使用最上層或快顯視窗。

應用程式可以指定 CS \_ PARENTDC 樣式，將子視窗的裁剪區域設定為父視窗的裁剪區域，讓子視窗可以在父系中繪製。 指定 CS \_ PARENTDC 可增強應用程式的效能，因為系統不需要持續重新計算每個子視窗的可見區域。

父視窗所設定的屬性值不會保留給子視窗;例如，父視窗無法設定其子視窗的筆刷。 唯一保留的屬性是裁剪區域。 視窗必須將本身的輸出裁剪至視窗的限制。 因為父裝置內容的裁剪區域與父視窗相同，所以子視窗可能會在整個父視窗上繪製，但不能以這種方式使用父裝置內容。

如果父視窗 \_ 使用私用或類別裝置內容，系統會忽略 CS PARENTDC 樣式，如果父視窗裁剪其子視窗，或子視窗裁剪其子視窗或同級視窗。

 

 



