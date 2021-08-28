---
description: 本主題將告訴您如何控制動詞可視性。
title: 如何隱藏和控制動詞可見度
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c92455a87b971d50e7a5d48890a0dcf54dbd5b2acc0cf8245e3ee01c99987246
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119395838"
---
# <a name="how-to-suppress-and-control-verb-visibility"></a>如何隱藏和控制動詞可見度

本主題將告訴您如何控制動詞可視性。

## <a name="instructions"></a>指示


您可以使用 Windows 原則設定來控制動詞可視性。 藉由將 **SuppressionPolicy** 子機碼或 **SuppressionPolicyEx** GUID 值新增至動詞的登錄子機碼，就可以透過原則設定來隱藏動詞命令。 將 **SuppressionPolicy** 子機碼的值設定為原則識別碼。 如果原則已開啟，則會隱藏動詞和其相關聯的快捷方式功能表項目。 如需可能的原則識別碼值，請參閱 [**限制**](/windows/desktop/api/shlobj_core/ne-shlobj_core-restrictions) 列舉。

 

 



