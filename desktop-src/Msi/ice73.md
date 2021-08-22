---
description: ICE73 會確認您的套件未重複使用封裝程式碼、升級程式碼或 Windows Installer SDK 範例的產品代碼。 套件永遠不應該重複使用另一個產品的封裝、升級或產品代碼。
ms.assetid: a04429c2-ff9e-4ec8-8d07-faf1479f4920
title: ICE73
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f2e5beecbfc7b4345d3b0dd7a93b86c55acc1abde4cc4f99d72749368be9d303
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118635074"
---
# <a name="ice73"></a>ICE73

ICE73 會確認您的套件未重複使用封裝程式碼、升級程式碼或 Windows Installer SDK 範例的產品代碼。 套件永遠不應該重複使用另一個產品的封裝、升級或產品代碼。

## <a name="result"></a>結果

如果您的產品套件重複使用 Windows Installer SDK 範例的封裝或產品代碼，ICE73 會輸出警告。

## <a name="example"></a>範例

ICE73 會針對所顯示的範例報告下列錯誤：

``` syntax
This package reuses the '{80F7E030-A751-11D2-A7D4-006097C99860}' ProductCode of the orca.msi 1.0 Windows Installer SDK package.
This package reuses the '{000C1101-0000-0000-C000-000000000047}' Package Code of the msispy.msi 1.0 Windows Installer SDK package.
This package reuses the '{8FC7****-88A0-4b41-82B8-8905D4AA904C}' Upgrade Code of a 1.1 Windows Installer SDK package.
```

> [!Note]  
> GUID 中的星號 (\* \* \* \*) 代表針對後續 Windows Installer SDK 套件保留的 guid 範圍。

 

若要修正錯誤，請針對套件的產品和套件代碼產生新的唯一 GUID。 您也需要套件升級程式碼的新唯一 GUID。

[摘要資訊串流](summary-information-stream.md) (部分) 



| 屬性       | 值                                  |
|----------------|----------------------------------------|
| PID \_ REVNUMBER | {000C1101-0000-0000-C000-000000000047} |



 

[屬性工作表](property-table.md) (部分) 



| 屬性                           | 值                                  |
|------------------------------------|----------------------------------------|
| [**ProductCode**](productcode.md) | {80F7E030-A751-11D2-A7D4-006097C99860} |
| [**UpgradeCode**](upgradecode.md) | {8FC70000-88A0-4b41-82B8-8905D4AA904C} |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[封裝碼](package-codes.md)
</dt> <dt>

[產品代碼](product-codes.md)
</dt> <dt>

[**修訂編號摘要屬性**](revision-number-summary.md)
</dt> <dt>

[**UpgradeCode 屬性**](upgradecode.md)
</dt> <dt>

[**ProductCode 屬性**](productcode.md)
</dt> <dt>

[ICE 參考](ice-reference.md)
</dt> </dl>

 

 



