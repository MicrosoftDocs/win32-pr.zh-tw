---
description: 針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。
ms.assetid: bf3ca2b0-a9fb-4e63-87de-6d5cbe5cd746
title: Bit-Flag 資料常數
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 238627505bf414ed0ab94ff2f5c35197705c91d1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106989317"
---
# <a name="bit-flag-data-constants"></a>Bit-Flag 資料常數

針對可延伸位旗標資料常數，服務提供者廠商可以定義指定位的新值。 因為大部分位旗標常數都是 **DWORD**，所以較低位的特定數目通常會保留給一般擴充，而其餘的位則適用于廠商專屬的延伸模組。 一般位旗標是從位零開始指派，而廠商專屬的延伸模組則應從位31下指派。 此配置提供最大的彈性，可將位位置指派給通用擴充功能，而不是廠商專屬的延伸模組。 廠商預期會定義新的值，這些值是 API 所定義之位旗標的自然延伸。

可擴充的資料結構具有大小可變大小的欄位，保留給裝置特定用途。 因為欄位是大小可變大小，所以服務提供者會決定欄位的資訊和轉譯量。 定義裝置特定欄位的廠商預期會讓 API 所定義的原始資料結構自然擴充。

 

 



