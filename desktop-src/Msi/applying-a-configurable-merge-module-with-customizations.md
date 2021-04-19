---
description: 遵循套用合併模組中所述套用合併模組的一般方針。
ms.assetid: 6035b1a9-d452-4020-9fe3-c20ba874a2ed
title: 套用可設定的合併模組與自訂
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: c4f1e3da426ba5ca13e149814ab9bb927e83d4e2
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106977043"
---
# <a name="applying-a-configurable-merge-module-with-customizations"></a>套用可設定的合併模組與自訂

遵循套用 [合併模組](applying-merge-modules.md)中所述套用合併模組的一般方針。 此外，合併模組取用者必須執行下列動作，才能在安裝時設定合併模組：

-   使用為了具有可設定的設定而撰寫的合併模組。 如需詳細資訊，請參閱[建立可由終端使用者設定的合併模組](creating-a-merge-module-that-can-be-configured-by-the-end-user.md)。
-   使用可呼叫 Mergemod.dll 2.0 版或更新版本的「合併和設定」工具。 舊版的 Mergmod.dll 無法設定合併模組設定。 作者應該建立可提供預設值且與舊版 Mergmod.dll 相容的合併模組。
-   在設定用戶端工具出現提示時提供自訂資訊。 當使用者拒絕提供資訊時，作者應建立使用預設值的合併模組。

 

 



