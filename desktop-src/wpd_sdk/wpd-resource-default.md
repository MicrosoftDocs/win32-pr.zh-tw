---
description: 指定物件後方的整個檔案。 它也是參考任何資源類型的方式，包括其他 Windows 可攜式裝置資源類型未涵蓋的資源類型，例如自訂物件類型。
ms.assetid: e534ea86-4932-45c7-87e7-03926202fa7e
title: WPD_RESOURCE_DEFAULT
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: 2d939cf58033baded231363b39410c2e527fe303075c94255a00ba96831a609b
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "119805878"
---
# <a name="wpd_resource_default"></a>WPD \_ 資源 \_ 預設

指定物件後方的整個檔案。 它也是參考任何資源類型的方式，包括其他 Windows 可攜式裝置資源類型未涵蓋的資源類型，例如自訂物件類型。

將包含內嵌于指定資源內的任何資源。 例如，連絡人根資料夾的預設資源可能包含所有嵌套的連絡人。 但是，任何僅由中繼資料或參考所 *連結* 的子資源都不會包含在內。 其中一個範例就是播放清單，它可能只會透過中繼資料參考或檔案中的文字路徑參考連結到音訊檔案。

此 **PROPERTYKEY** 唯一允許的 *pid* 值為零。

這種類型的資源必須支援下列屬性。



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

 

 



