---
description: 針對 NLS，排序 (也稱為 &\# 0034; 定序&\# 0034; ) 是字串的相片順序。
ms.assetid: 8ca3af60-1ddb-4bfb-8aa6-8db769b3982d
title: '排序 (國際化) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: f3dbedf872c953a45ca7064eccd4ba16019a857c35186261695e094be03cd054
ms.sourcegitcommit: e6600f550f79bddfe58bd4696ac50dd52cb03d7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/11/2021
ms.locfileid: "120130208"
---
# <a name="sorting"></a>排序

針對 NLS，排序 (也稱為「定序」 ) 是字串的相片順序。 排序有兩種類型：

-   語言排序。 依) 排序，將具有類似語言特性的字串排列成群組 (。
-   序數 (非語言) 排序。 依排序次序排列字串。

排序會使用 NLS 字串比較函式（例如 [CompareString](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw) 和 [**LCMapString**](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)）或「包裝函式」 API 函式（例如 [lstrcmp](/windows/win32/api/winbase/nf-winbase-lstrcmpa)），在內部呼叫 NLS 字串比較函數。

如需在應用程式中執行排序的詳細資訊，請參閱 [在您的應用程式中處理排序](handling-sorting-in-your-applications.md)。

## <a name="related-topics"></a>相關主題

<dl> <dt>

[關於國家語言支援](about-national-language-support.md)
</dt> <dt>

[處理應用程式中的排序](handling-sorting-in-your-applications.md)
</dt> <dt>

[**CompareString**](/windows/win32/api/stringapiset/nf-stringapiset-comparestringw)
</dt> <dt>

[LCMapString](/windows/desktop/api/Winnls/nf-winnls-lcmapstringa)
</dt> </dl>

 

 
