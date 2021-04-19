---
title: 叫用 MIDL 編譯器
description: MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。 請參閱/target 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。
ms.assetid: 57730efa-71c3-4746-83f4-c7e327888efc
keywords:
- MIDL 編譯器 MIDL，叫用
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 3b7e03abc49007b823f509acb35bd34ce6e47d80
ms.sourcegitcommit: 1e8e6e6f27c909900cfa8be58b042456331a82ad
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/15/2019
ms.locfileid: "106976329"
---
# <a name="invoking-the-midl-compiler"></a>叫用 MIDL 編譯器

MIDL 編譯器可以針對不同的平臺和系統版本產生程式碼。 請參閱 [**/target**](-target.md) 參數，以深入瞭解建議的參數，以及如何產生針對特定版本優化的程式碼。

使用下列命令，從命令列執行 MIDL 編譯器：

**midl** *< 選項 >* **filename .idl**

其中 *< 選項 >* 代表您要使用的命令列選項，而 Filename 則是要編譯之 MIDL 檔案的名稱。

當您使用 MIDL 編譯器 [**/help**](-help-.md) 和/？時，可使用 midl 編譯器參數和選項的完整清單。 開關。 這些參數是依類別目錄組織。 如需詳細資訊，請參閱 [MIDL Command-Line 參考](midl-command-line-reference.md)。

> [!NOTE]
> 新的 global 旗標 **$ (MIDL \_ 優化)** 存在於 win32 中。 使用此旗標編譯 .idl 檔案時，產生的存根可以利用指定平臺上可用的最新 RPC 功能，並可能改善應用程式的效能和穩定性。 使用 MIDL 時，建議應用程式使用這個旗標。
>
> **midl** **$ (midl \_ 優化)** **...**