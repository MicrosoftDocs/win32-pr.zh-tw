---
description: 指定 Windows 可攜式裝置未以其他方式定義的資源類型。
ms.assetid: a4d812fe-f050-450a-acee-20b4152e8d76
title: WPD_RESOURCE_GENERIC
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: c418299474373d8b960d15c429ea98d887cc404be49c8d38c7d2bb83611c4ca1
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805868"
---
# <a name="wpd_resource_generic"></a>WPD \_ 資源 \_ 泛型

指定 Windows 可攜式裝置未以其他方式定義的資源類型。 您可以定義自己的自訂資源，以支援任何自訂或 Windows 便攜裝置定義的屬性。 不過，您所建立的任何資源都必須支援下列屬性。



| 屬性名稱                                                                                                            | 必要或選擇性                                   |
|---------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------|
| [WPD \_ 資源 \_ 屬性 \_ 總 \_ 大小](resource-attribute-properties.md)              | 必要。                                              |
| [WPD \_ 資源 \_ 屬性 \_ 可以 \_ 讀取](attributes.md)                                     | 如果用戶端可以讀取此資源，則為必要。            |
| [WPD \_ 資源 \_ 屬性 \_ 可以 \_ 寫入](attributes.md)                                   | 如果用戶端可以寫入此資源，則為必要。        |
| [WPD \_ 資源 \_ 屬性 \_ 可以 \_ 刪除](attributes.md)                                 | 如果用戶端可以刪除此資源，則為必要。          |
| [WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 讀取 \_ 緩衝區 \_ 大小](attributes.md)   | 如果用戶端擁有資源的讀取權限，則為必要。  |
| [WPD \_ 資源 \_ 屬性 \_ 最佳 \_ 寫入 \_ 緩衝區 \_ 大小](attributes.md) | 如果用戶端具有資源的寫入權限，則為必要。 |
| [WPD \_ 資源 \_ 屬性 \_ 格式](resource-attribute-properties.md)                       | 必要。                                              |
| [WPD \_ 資源 \_ 屬性 \_ 資源 \_ 金鑰](resource-attribute-properties.md)                                              | 建議使用。                                           |



 

## <a name="see-also"></a>另請參閱

<dl> <dt>

[**資源的需求**](requirements-for-resources.md)
</dt> </dl>

 

 



