---
description: 如果每個使用者的系統原則設定為 &\# 0034; 1&\# 0034; 則執行某項產品維護安裝的使用者和系統管理員，將無法使用 [流覽] 對話方塊來流覽媒體來源（如 cd-rom），以取得其他可安裝產品的來源。
ms.assetid: 275a6d43-ecf8-4146-82eb-3b42b25b9a80
title: DisableMedia
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: d2337a1698865b0b977e179021f6490e2fa651a8c4baa3a56e808d037926ad39
ms.sourcegitcommit: e858bbe701567d4583c50a11326e42d7ea51804b
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "118143244"
---
# <a name="disablemedia"></a>DisableMedia

如果每個使用者的 [系統原則](system-policy.md) 設定為 "1"，則執行某項產品之維護安裝的使用者和系統管理員，將無法使用 [流覽] 對話方塊來流覽其他可安裝產品來源的媒體來源，例如 cd-rom。 無論是否以較高的許可權進行安裝，都會防止流覽其他產品。 如果使用者已正確標示媒體來源，則使用者仍然可以從媒體重新安裝產品。

## <a name="registry-key"></a>登錄金鑰

**HKEY \_\_** \\  \\  \\ **Microsoft** \\ **Windows** \\ **安裝程式** 的目前使用者軟體原則

## <a name="data-type"></a>資料類型

**REG \_ DWORD**

## <a name="remarks"></a>備註

請注意， [**DISABLEMEDIA**](-disablemedia.md) 屬性與 DISABLEMEDIA 原則的效果不同。 設定 DisableMedia 系統原則，只會停用流覽至媒體來源。 設定 **DISABLEMEDIA** 屬性可防止安裝程式將任何媒體來源（例如 cd-rom）註冊為產品的有效來源。 但是，如果已啟用流覽，使用者仍可流覽至媒體來源。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[來源復原](source-resiliency.md)
</dt> </dl>

 

 



