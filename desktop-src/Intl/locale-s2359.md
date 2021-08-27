---
description: 地區設定 \_ S2359 和地區設定 \_ SPM
ms.assetid: 8a97073e-84f6-47d9-98fb-65760e8a6cd8
title: LOCALE_S2359 和 LOCALE_SPM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8690d40907135b88966286c8cb36cf72cf31f372ba2160fc6d49637ac813129d
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106318"
---
# <a name="locale_s2359-and-locale_spm"></a>地區設定 \_ S2359 和地區設定 \_ SPM

PM 指示項的字串 (第一天的12小時) 。 針對不同版本的 Windows，此字串允許的字元數上限不同。

**Windows XP：** 十三包含 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)的終止 null 字元。 15包含 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)的終止 null 字元。

**Windows Me/98/95、Windows NT 4.0 Windows 2000：** 九個包含終止的 null 字元。

**Windows Server 2003 和更新版本：** 15個包含終止的 null 字元。

Windows 10 新增了值 **地區設定 \_ SPM** ，作為 **地區設定 \_ S2359** 更容易閱讀的同義字。

 

 



