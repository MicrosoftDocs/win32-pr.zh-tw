---
description: 安裝到全域組件快取的 Common language runtime 元件，在所有出現的元件中都必須有相同的檔案。
ms.assetid: 02b4ad60-d28d-44b8-955f-b367197e69c3
title: Common Language Runtime 元件的重新安裝模式
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 8512e4c6e888c7d67b2ca252184fa4f748445fb8
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106974665"
---
# <a name="reinstallation-modes-of-common-language-runtime-assemblies"></a>Common Language Runtime 元件的重新安裝模式

安裝到全域組件快取的 Common language runtime 元件，在所有出現的元件中都必須有相同的檔案。 這表示 [**MsiReinstallFeature**](/windows/desktop/api/Msi/nf-msi-msireinstallfeaturea) 和 [**MsiReinstallProduct**](/windows/desktop/api/Msi/nf-msi-msireinstallproducta) 所使用的重新安裝模式必須對一般元件和 common language runtime 元件具有不同的意義。 下列重新安裝模式的定義適用于 common language runtime 元件。



| 重新安裝模式                  | Microsoft .NET 元件的意義                                                                                              |
|---------------------------------|------------------------------------------------------------------------------------------------------------------------------------|
| REINSTALLMODE \_ FILEMISSING      | 如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。                                         |
| REINSTALLMODE \_ FILEOLDERVERSION | 如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。                                         |
| REINSTALLMODE \_ FILEEQUALVERSION | 如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。                                         |
| REINSTALLMODE \_ FILEEXACT        | 如果 common language runtime 元件遺失或不完整，請安裝或重新安裝。                                         |
| REINSTALLMODE \_ FILEVERIFY       | 如果 common language runtime 元件遺失或現有元件不完整或已損毀，請安裝或重新安裝。 |
| REINSTALLMODE \_ FILEREPLACE      | 一律安裝或重新安裝 common language runtime 元件。                                                                 |



 

 

 



