---
title: 套用至參數的指標屬性
description: 每個指標屬性 ( \ ref \、\ unique \ 和 \ ptr \ ) 都有影響記憶體配置的特性。 下表摘要說明這些特性。
ms.assetid: 25a609cd-efe7-4cbb-b80e-b6a3ad8cda38
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0c7710fb3c39702b2b2fdb789ed1218dc88d44ea
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "104023923"
---
# <a name="pointer-attributes-applied-to-the-parameter"></a>套用至參數的指標屬性

每個指標屬性 (\[ [ref](/windows/desktop/Midl/ref) \] 、 \[ [unique](/windows/desktop/Midl/unique) \] 和 \[ [ptr](/windows/desktop/Midl/ptr) \]) 都有影響記憶體配置的特性。 下表摘要說明這些特性。



| 指標屬性       | 用戶端                                                                                                                                                                                                            | 伺服器                                                              |
|-------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------|
| 參考 (\[ **ref** \])  | 用戶端應用程式必須配置。                                                                                                                                                                                 | 僅限 **\[ out \]** nontop 層級指標所需的特殊處理。 |
| 唯一 (\[ **唯一** \])  | 如果是參數，用戶端應用程式必須配置;如果是內嵌的，可以是 null。 從 null 變更為非 null 會導致用戶端存根配置;從非 null 變更為 null 可能會導致損壞。<br/> |                                                                     |
| 完整 (\[ **ptr** \])       | 如果是參數，用戶端應用程式必須配置;如果是內嵌的，可以是 null。 從 null 變更為非 null 會導致用戶端存根配置;從非 null 變更為 null 可能會導致損壞。<br/> |                                                                     |



 

**\[ Ref \]** 屬性工作表示指標指向有效的記憶體。 根據定義，用戶端應用程式必須配置參考指標所需的所有記憶體。

唯一指標可從 null 變更為非 null。 如果唯一指標從 null 變更為非 null，則會在用戶端上配置新的記憶體。 如果唯一指標從非 null 變更為 null，則會產生損壞。 如需詳細資訊，請參閱 [記憶體損壞](memory-orphaning.md)。

 

