---
description: 地區設定 \_ SLONGDATE
ms.assetid: 1b72cd57-819e-4b1f-bbb0-b600a9e8631c
title: LOCALE_SLONGDATE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 33e47409d99d4db9afa2e684d3be8ae2f874200d56d748868eaa0fa1953452d4
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106058"
---
# <a name="locale_slongdate"></a>地區設定 \_ SLONGDATE

地區設定的完整日期格式字串。 此字串允許的最大字元數為80，包括結束的 null 字元。 字串可以包含 [day、month、year 和紀元格式的圖片](day--month--year--and-era-format-pictures.md) ，以及以單引號括住的任何字元字串。 以單引號括住的字元會維持指定的狀態。 例如，西班牙文 (西班牙) 的完整日期為 "dddd，dd ' de ' MMMM ' de ' yyyy"。 地區設定可以定義多個完整的日期格式。

若要取得地區設定的所有完整日期格式，請使用 [EnumDateFormats](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsa)、 [EnumDateFormatsEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexa)或 [EnumDateFormatsExEx](/windows/desktop/api/Winnls/nf-winnls-enumdateformatsexex)。

 

 



