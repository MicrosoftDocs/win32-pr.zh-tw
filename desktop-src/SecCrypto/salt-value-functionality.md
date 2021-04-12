---
description: 基底提供者會以零值 salt 的11個位元組建立40位的對稱金鑰，如果指定了 CRYPT CREATE salt，則會建立11個位元組的非零 salt， \_ \_ 或沒有 salt 值。
ms.assetid: f1af0af7-c64e-435a-aef0-7c4ed7bd1199
title: Salt 值功能
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: bd8e3049c431cf909c1008acac26925cd1fa9e6c
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104318715"
---
# <a name="salt-value-functionality"></a>Salt 值功能

基底提供者會以零值 [*salt*](../secgloss/s-gly.md)的11個位元組建立40位的 [*對稱金鑰*](../secgloss/s-gly.md)，如果指定了 CRYPT CREATE salt，則會建立11個位元組的非零 salt， \_ \_ 或沒有 salt 值。 不過，具有零值 salt 的40位對稱金鑰，不等於沒有 salt 的40位對稱金鑰。 基於互通性，您必須建立金鑰，而不需要 salt。 此問題的原因是預設條件只會與40位的索引鍵完全相符。 所有其他 [*金鑰長度*](../secgloss/k-gly.md) 預設不會配置 salt。

基底提供者和延伸提供者都可以使用 CRYPT \_ NO \_ SALT 旗標來指定為40位對稱金鑰配置 SALT 值。 接受此旗標的函式為 [**CryptGenKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptgenkey)、 [**CryptDeriveKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptderivekey)和 [**CryptImportKey**](/windows/desktop/api/Wincrypt/nf-wincrypt-cryptimportkey)。 根據預設，這些函式會繼續使用11位元組長的零值 salt，為40位對稱金鑰案例提供回溯相容性。

 

 
