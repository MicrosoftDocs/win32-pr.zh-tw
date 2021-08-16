---
description: 使用以 null 結束的字串時，您的 Unicode 應用程式應該一律將零轉換成 TCHAR。
ms.assetid: 43bbf0ab-9b69-4f7d-acda-d0f8b6caf4b5
title: 使用以 Null 結尾的字串
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7d0a5f27048bde2af75eca28626a562473ceffcc66f3f2f23509beca4fba06ba
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119631778"
---
# <a name="using-null-terminated-strings"></a>使用以 Null 結尾的字串

使用以 null 結束的字串時，您的 Unicode 應用程式應該一律將零轉換成 TCHAR。 程式碼0x0000 是以 null 終止之字串的 Unicode 字串結束字元。 單一 null 位元組對此程式碼而言不足，因為許多 Unicode 字元都包含 null 位元組做為高或低位元組。 其中一個範例是字母 A，其字元碼為0x0041。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[使用 Unicode 中的特殊字元](using-special-characters-in-unicode.md)
</dt> </dl>

 

 



