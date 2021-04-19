---
description: MTP 延伸模組屬性
ms.assetid: 58fc8741-261a-4e63-9fd3-8f0ca05866ad
title: MTP 延伸模組屬性
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 86a653d05285d62c7660bd914a785807a2341a01
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/08/2021
ms.locfileid: "106996783"
---
# <a name="mtp-extension-properties"></a>MTP 延伸模組屬性

屬性會描述物件、屬性、資源和裝置。

## <a name="vendor-extended-object-properties"></a>廠商-擴充的物件屬性

當裝置製造商建立裝置物件的廠商擴充屬性時，會將 **WPD \_ PROPERTIES \_ MTP \_ 廠商 \_ 擴充 \_ 物件 \_ .props** GUID 與物件的屬性程式碼結合，以建立 **PROPERTYKEY** 結構。

例如，如果物件的屬性程式碼是0xD801，則產生的 **PROPERTYKEY** 會如下列範例所示：


```C++
{4D545058-4FCE-4578-95C8-8698A9BC0F49}\D801
```



## <a name="vendor-extended-device-properties"></a>廠商延伸的裝置屬性

當裝置製造商建立裝置的廠商擴充屬性時，會將 **WPD \_ 屬性 \_ MTP \_ 廠商 \_ 擴充 \_ 裝置 \_ .props** GUID 與物件的屬性程式碼結合，以建立 **PROPERTYKEY** 結構。

例如，如果物件的屬性程式碼是0xD001，則產生的 **PROPERTYKEY** 會如下列範例所示：


```C++
{4D545058-8900-40b3-8F1D-DC246E1E8370}\D001
```



## <a name="related-topics"></a>相關主題

<dl> <dt>

[支援 MTP 擴充功能](supporting-mtp-extensions.md)
</dt> </dl>

 

 



