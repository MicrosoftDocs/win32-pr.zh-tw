---
title: 'VariantNotInt (CheckRole) '
description: 'VariantNotInt (CheckRole) '
ms.assetid: 24A9E91D-92E6-492B-B5CE-DF42E5923F60
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: fdca744468d863ff1ab95b66edf5b3ff1f40b48f
ms.sourcegitcommit: 2d531328b6ed82d4ad971a45a5131b430c5866f7
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/16/2019
ms.locfileid: "104300988"
---
# <a name="variantnotint-checkrole"></a>VariantNotInt (CheckRole) 

## <a name="text"></a>Text

從傳回的變異數 {0} 應為， {1} 但為 {2} 。

## <a name="type"></a>類型

錯誤

## <a name="description"></a>描述

元素報告了不正確 MSAA 角色。 例如，用來取出專案之 MSAA 角色的 [**get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole) 方法，應該傳回代表其中一個 msaa 角色常數的整數值，但改為傳回另一個 variant。

這個問題會讓依賴螢幕讀取器和鍵盤進行流覽的人員遇到問題，因為專案可能會不正確地識別給使用者。

## <a name="possible-causes"></a>可能的原因

元素或其父系的 MSAA 角色設定不當。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[**IAccessible：： get \_ accRole**](/windows/desktop/api/Oleacc/nf-oleacc-iaccessible-get_accrole)
</dt> <dt>

[**物件角色**](object-roles.md)
</dt> </dl>

 

 




