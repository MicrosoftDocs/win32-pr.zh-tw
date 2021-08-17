---
description: 憑證服務支援 CA) 階層的憑證授權單位單位 (。
ms.assetid: bcae26cd-41bc-4436-8f8b-cd8c20e9fcfc
title: 階層
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 240f2f2fc2920db1a67adb18281ad5c1d67fabdb2996ae3aae8342f96b1810c1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119006296"
---
# <a name="hierarchies"></a>階層

憑證服務支援 CA) 階層的 [*憑證授權單位*](../secgloss/c-gly.md) 單位 (。 [*Ca*](../secgloss/c-gly.md)階層是由最上層 ca 所組成， (稱為「根 ca) ，其中包含一個或多個由根 ca 發行憑證的次級 ca。 可能的 CA 階層案例會在具有一個根 CA 的組織中，用來將憑證發行給數個從屬 Ca。 次級 Ca 接著可以發出終端實體憑證，例如發給使用者的憑證。 使用者的憑證將包含 CA 階層的信任路徑，在此情況下，包含發行的次級 CA 和根 CA 的憑證。

 

 
