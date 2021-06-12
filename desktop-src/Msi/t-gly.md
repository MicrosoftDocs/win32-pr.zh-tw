---
description: 瞭解以字母 T 開頭的 Windows Installer 概念，例如交易處理和轉換。
ms.assetid: 06fd0284-5af9-409a-8748-c0b40e0fa317
title: 'T (Windows Installer) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 7e9489455f880ba558e5a9f8584be19718823035
ms.sourcegitcommit: 8f0a1d212dd154e8d94ab4c0e4ced053fa16823a
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/11/2021
ms.locfileid: "112011261"
---
# <a name="t-windows-installer"></a>T (Windows Installer) 

[](a-gly.md) [B](b-gly.md) [C](c-gly.md) [D](d-gly.md) [E](e-gly.md) [F](f-gly.md) [G](g-gly.md) H [I](i-gly.md) J K L [M](m-gly.md) N [O](o-gly.md) [P](p-gly.md) [Q](q-gly.md) [R](r-gly.md) [S](s-gly.md) [T W](u-gly.md) [](v-gly.md) X Y Z

<dl> <dt>

<span id="_msi_transaction_processing_gly"></span><span id="_MSI_TRANSACTION_PROCESSING_GLY"></span>**交易處理**
</dt> <dd>

一或多個作業會一起處理為單一不可分割，稱為「交易」。 所有組成的作業都必須成功，交易才會成功，否則所有作業都會回復為原始狀態。

</dd> <dt>

<span id="_msi_transform_gly"></span><span id="_MSI_TRANSFORM_GLY"></span>**變換**
</dt> <dd>

您可以套用的兩個 [*安裝程式資料庫*](i-gly.md) 之間的差異範本，以在其他資料庫產生類似的變更。 例如，當地語系化轉換可以用來變更應用程式的語言。 如需詳細資訊，請參閱 [合併和轉換](merges-and-transforms.md)。

</dd> <dt>

<span id="_msi_transform_error_condition_flags_gly"></span><span id="_MSI_TRANSFORM_ERROR_CONDITION_FLAGS_GLY"></span>**轉換錯誤條件旗標**
</dt> <dd>

用來標示 [*轉換*](/windows)之錯誤狀況的屬性集。 如需詳細資訊，請參閱 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)。

</dd> <dt>

<span id="_msi_transform_validation_flags_gly"></span><span id="_MSI_TRANSFORM_VALIDATION_FLAGS_GLY"></span>**轉換驗證旗標**
</dt> <dd>

用來確認 [*轉換*](/windows) 可以套用至資料庫的屬性集。 如需這些屬性的清單，請參閱 [**MsiCreateTransformSummaryInfo**](/windows/desktop/api/Msiquery/nf-msiquery-msicreatetransformsummaryinfoa)。

</dd> </dl>

 

 
