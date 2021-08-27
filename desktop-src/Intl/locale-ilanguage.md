---
description: 地區設定 \_ ILANGUAGE
ms.assetid: 8f80a941-8ba6-4a0d-92fa-77230fe0a9d1
title: LOCALE_ILANGUAGE
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3159fe26ce1af7291c5990a07297e7513144b5187b55c00086bf46e452ef188c
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120106648"
---
# <a name="locale_ilanguage"></a>地區設定 \_ ILANGUAGE

具有十六進位值的[語言識別項](language-identifiers.md)。 例如，英文 (美國) 的值為0409，表示0x0409 十六進位，相當於 1033 decimal。 此字串允許的最大字元數為五個字元，包括結束的 null 字元。

**Windows Vista 和更新版本：** 使用這個常數可能會導致 [**GetLocaleInfo**](/windows/desktop/api/Winnls/nf-winnls-getlocaleinfoa)傳回不正確地區設定識別碼。 呼叫此函式時，您的應用程式應該使用 [LOCALE \_ SNAME](locale-sname.md) 常數。

 

 



