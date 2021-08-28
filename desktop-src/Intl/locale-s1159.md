---
description: 地區設定 \_ S1159 和地區設定 \_ SAM
ms.assetid: dc7058af-1d5f-40a0-8d0b-17d2ff5662ce
title: LOCALE_S1159 和 LOCALE_SAM
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 690132c0eb56dc75dd34eae217a6fa7598256852ef4e7039cc988754f7a589f2
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106338"
---
# <a name="locale_s1159-and-locale_sam"></a>地區設定 \_ S1159 和地區設定 \_ SAM

AM 指示項的字串 (一天中的前12小時) 。 針對不同版本的 Windows，此字串允許的最大字元數（包括結束的 null 字元）會有所不同。

**Windows XP：** 十三包含 [**SetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-setlocaleinfoa)的終止 null 字元。 15包含 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)的終止 null 字元。

**Windows Me/98/95、Windows NT 4.0 Windows 2000：** 九個包含終止的 null 字元。

**Windows Server 2003 和更新版本：** 15個包含終止的 null 字元。

Windows 10 為 **地區設定 \_ S1159** 新增了值 **地區設定 \_ SAM** 作為更容易閱讀的同義字。

 

 



