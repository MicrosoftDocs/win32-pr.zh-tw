---
title: 伺服器如何執行子系識別碼
description: 伺服器開發人員可以將子識別碼指派給簡單的元素和可存取的物件。 不過，建議的方法是在每個具有子系的可存取物件中，支援標準元件物件模型 (COM) 介面 IEnumVARIANT。
ms.assetid: 236de46e-8fe0-4f53-b989-267c9ee87545
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 0721c9660aa02fb16e9ec33495279cd90e872a37
ms.sourcegitcommit: 592c9bbd22ba69802dc353bcb5eb30699f9e9403
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/20/2020
ms.locfileid: "103933411"
---
# <a name="how-servers-implement-child-ids"></a>伺服器如何執行子系識別碼

伺服器開發人員可以將子識別碼指派給簡單的元素和可存取的物件。 不過，建議的方法是在每個具有子系的可存取物件中，支援標準元件物件模型 (COM) 介面 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 。

如果您執行 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)，則必須：

-   列舉所有子系，簡單元素和可存取的物件都是。 為所有簡單的專案提供子系識別碼，並將 [**IDispatch**](idispatch-interface.md) 提供給每個可存取的物件。
-   針對可存取的物件，將 [**VARIANT**](variant-structure.md)的 **vt** 成員設定為 vt \_ 分派。 **PdispVal** 成員必須包含 [**IDispatch**](idispatch-interface.md)介面的指標。 請注意， **變數** 會由用戶端配置及釋放。
-   針對簡單的專案，子系識別碼為任何32位正整數。 請注意，Microsoft Active Accessibility 會保留零和負整數。 將 [**VARIANT**](variant-structure.md) 結構 **vt** 成員設定為 vt \_ I4，並將 **LVAL** 成員設定為子系識別碼。

如果您不支援 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant)，則必須在每個物件中，依序從1開始指派子系識別碼和子系的編號。

建議用戶端使用 Microsoft Active Accessibility 函數 [**AccessibleChildren**](/windows/desktop/api/Oleacc/nf-oleacc-accessiblechildren) ，而不是直接呼叫伺服器 [IEnumVARIANT](/windows/win32/api/oaidl/nn-oaidl-ienumvariant) 介面。

 

 