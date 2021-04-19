---
description: ICE80 會驗證範本摘要屬性 (PID 範本的值 \_) 正確地指定 &\# 0034; Intel64&\# 0034;，&\# 0034; x64&\# 0034; 或 &\# 0034; Intel&\# 0034; 視64位元件或自訂動作腳本的存在而定。
ms.assetid: fd2a15cf-d117-4a87-a26e-caff4b12a2e9
title: ICE80
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5d5233f260e9cc248bdb2d0c19b47956a2b7dbe1
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "106999862"
---
# <a name="ice80"></a>ICE80

ICE80 會驗證 [**範本摘要**](template-summary.md) 屬性 (PID 範本的值 \_) 正確地指定 "Intel64"、"x64"、"Arm64" 或 "Intel"，視64位元件或自訂動作腳本的存在而定。 ICE80 會使用 **msidbComponentAttributes64bit** 屬性檢查 [元件資料表](component-table.md)中是否有任何元件，並檢查 [CustomAction 資料表](customaction-table.md)中是否有 **msidbCustomActionType64BitScript** 屬性的任何腳本。 ICE80 會確認 **範本摘要** 屬性中具有 "Intel64"、"x64" 或 "Arm64" 的封裝，也有 [ [**頁面計數摘要**](page-count-summary.md) ] 屬性 (PID \_ PAGECOUNT) 至少為150。

ICE80 也會驗證 [**ProductLanguage**](productlanguage.md) 屬性指定的語言識別項必須包含在 [**範本摘要**](template-summary.md) 屬性中。

如需詳細資訊，請參閱 [64 位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)。

## <a name="result"></a>結果

ICE80 會張貼下列錯誤。



| 錯誤                                                                                                                                                                   | 描述                                                                                                                                                                                                               |
|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| 此封裝包含64位元件 ' \[ 1 \] '，但 [**範本摘要**](template-summary.md) 屬性不包含 Intel64、x64 或 Arm64。                    | [元件資料表](component-table.md)包含具有 **msidbComponentAttributes64bit** 屬性的元件，而 [**範本摘要**](template-summary.md)屬性不包含 Intel64、x64 或 Arm64。        |
| 此封裝包含64位自訂動作腳本 ' \[ 1 \] '，但 [**範本摘要**](template-summary.md) 屬性不包含 Intel64、x64 或 Arm64。         | [CustomAction 資料表](customaction-table.md) 包含使用 **msidbCustomActionType64BitScript** 的腳本自訂動作，但 [**範本摘要**](template-summary.md) 屬性不包含 Intel64、x64 或 Arm64。 |
| % S 的摘要資訊資料流程中的值錯誤。                                                                                                                         | \_如果該屬性是空字串或非 VT LPSTR 類型，則會針對 PID 範本屬性傳回 \_ 。 針對 PID \_ PAGECOUNT 傳回，如果該屬性不是 VT \_ I4 類型。<br/>                                         |
| 此封裝已標示為 Intel64，但其架構小於150。                                                                                                  | 封裝的 PID \_ 範本屬性為 Intel64，但其 pid \_ PAGECOUNT 屬性小於150。                                                                                                            |
| 此封裝以 x64 標記，但其架構小於200。                                                                                                      | 封裝的 PID \_ 範本屬性為 x64，但其 pid \_ PAGECOUNT 屬性小於200。                                                                                                            |
| 此封裝已標示為 Arm64，但其架構小於500。                                                                                                    | 封裝的 PID \_ 範本屬性為 Arm64，但其 pid \_ PAGECOUNT 屬性小於500。                                                                                                            |
| 此32位套件使用64位屬性 \[ 1\]                                                                                                                       | 32位封裝使用64位的屬性。                                                                                                                                                                              |
| 此32位套件在 RegLocator 資料表專案1中使用64位定位器類型 \[\]                                                                                         | 32位封裝在 [RegLocator 資料表](reglocator-table.md)的類型欄位中包含 **msidbLocatorType64bit** 。                                                                                                    |
| 此 64BitComponent \[ 1 \] 使用 32BitDirectory \[ 3\]                                                                                                                     | 64位元件正在使用32位目錄。                                                                                                                                                                           |
| 此 32BitComponent \[ 1 \] 使用 64BitDirectory \[ 3\]                                                                                                                     | 32位元件正在使用64位目錄。                                                                                                                                                                           |
| 屬性資料表中的 '[**ProductLanguage**](productlanguage.md)' 屬性的值為 ' \[ 2 \] '，其不包含在範本摘要屬性資料流程中。 | [ [**ProductLanguage**](productlanguage.md) ] 屬性的值未列在 [ [**範本摘要**](template-summary.md) ] 屬性中。                                                                          |



 

## <a name="related-topics"></a>相關主題

<dl> <dt>

[ICE 參考](ice-reference.md)
</dt> <dt>

[64位作業系統上的 Windows Installer](windows-installer-on-64-bit-operating-systems.md)
</dt> </dl>

 

 




