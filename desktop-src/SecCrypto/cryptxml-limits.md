---
description: CryptXML 會定義 Cryptxml .h 標頭檔中的下列全域限制。
ms.assetid: 8f4dc314-76fc-40ce-a1e1-a701ae39d66d
title: 'CryptXML 限制 (Cryptxml) '
ms.topic: reference
ms.date: 05/31/2018
ms.openlocfilehash: ccc56ee6459be2160efdeb8e9874e7dd0c53518d
ms.sourcegitcommit: 831e8f3db78ab820e1710cede244553c70e50500
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/07/2021
ms.locfileid: "104468885"
---
# <a name="cryptxml-limits"></a><span data-ttu-id="a95b9-103">CryptXML 限制</span><span class="sxs-lookup"><span data-stu-id="a95b9-103">CryptXML Limits</span></span>

<span data-ttu-id="a95b9-104">CryptXML 會定義 Cryptxml .h 標頭檔中的下列全域限制。</span><span class="sxs-lookup"><span data-stu-id="a95b9-104">CryptXML defines the following global limits in the Cryptxml.h header file.</span></span>



| <span data-ttu-id="a95b9-105">常數/值</span><span class="sxs-lookup"><span data-stu-id="a95b9-105">Constant/value</span></span>                                                                                                                                                                                                                                                             | <span data-ttu-id="a95b9-106">Description</span><span class="sxs-lookup"><span data-stu-id="a95b9-106">Description</span></span>                                                                                                                                                                                                                           |
|:---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|:--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| <span id="CRYPT_XML_BLOB_MAX"></span><span id="crypt_xml_blob_max"></span><dl> <span data-ttu-id="a95b9-107"><dt>**CRYPT \_XML \_ BLOB \_ MAX**</dt> <dt>0x7FFFFFF8</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-107"><dt>**CRYPT\_XML\_BLOB\_MAX**</dt> <dt>0x7FFFFFF8</dt></span></span> </dl>                             | <span data-ttu-id="a95b9-108">編碼的資料不能超過 2 gb 的 (GB) 。</span><span class="sxs-lookup"><span data-stu-id="a95b9-108">Encoded data cannot exceed 2 gigabytes (GB).</span></span><br/>                                                                                                                                                                               |
| <span id="CRYPT_XML_ID_MAX"></span><span id="crypt_xml_id_max"></span><dl> <span data-ttu-id="a95b9-109"><dt>**CRYPT \_XML \_ 識別碼 \_ 最大值**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-109"><dt>**CRYPT\_XML\_ID\_MAX**</dt> <dt>256</dt></span></span> </dl>                                          | <span data-ttu-id="a95b9-110">識別碼長度不能超過256個字元。</span><span class="sxs-lookup"><span data-stu-id="a95b9-110">Id length cannot exceed 256 characters.</span></span><br/>                                                                                                                                                                                    |
| <span id="CRYPT_XML_URI_MAX"></span><span id="crypt_xml_uri_max"></span><dl> <span data-ttu-id="a95b9-111"><dt>**CRYPT \_XML \_ URI \_ 最大值**</dt> <dt>8 \* 1024</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-111"><dt>**CRYPT\_XML\_URI\_MAX**</dt> <dt>8\*1024</dt></span></span> </dl>                                   | <span data-ttu-id="a95b9-112">URI 長度不能超過8192個字元。</span><span class="sxs-lookup"><span data-stu-id="a95b9-112">URI length cannot exceed 8192 characters.</span></span><br/>                                                                                                                                                                                  |
| <span id="CRYPT_XML_SIGNATURES_MAX"></span><span id="crypt_xml_signatures_max"></span><dl> <span data-ttu-id="a95b9-113"><dt>**CRYPT \_XML 簽章 \_ \_ 上限**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-113"><dt>**CRYPT\_XML\_SIGNATURES\_MAX**</dt> <dt>16</dt></span></span> </dl>                   | <span data-ttu-id="a95b9-114">每份 **檔的預設簽章元素數目** 上限。</span><span class="sxs-lookup"><span data-stu-id="a95b9-114">The default maximum number of **Signature** elements per document.</span></span> <span data-ttu-id="a95b9-115">將屬性值傳遞為 [**CRYPT \_ XML \_ 屬性**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) 結構時，可以指定新的最大值來覆寫這個值。</span><span class="sxs-lookup"><span data-stu-id="a95b9-115">This value can be overridden by specifying a new maximum when passing property values as [**CRYPT\_XML\_PROPERTY**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_property) structures.</span></span><br/> |
| <span id="CRYPT_XML_TRANSFORM_MAX"></span><span id="crypt_xml_transform_max"></span><dl> <span data-ttu-id="a95b9-116"><dt>**CRYPT \_XML \_ 轉換 \_ 上限**</dt> <dt>16</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-116"><dt>**CRYPT\_XML\_TRANSFORM\_MAX**</dt> <dt>16</dt></span></span> </dl>                      | <span data-ttu-id="a95b9-117">每個參考的轉換數目上限（以 [**CRYPT \_ xml \_ 演算法**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) 結構表示），以 [**CRYPT \_ xml \_ 參考**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) 結構表示。</span><span class="sxs-lookup"><span data-stu-id="a95b9-117">The maximum number of transforms, represented by [**CRYPT\_XML\_ALGORITHM**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_algorithm) structures, per reference, represented by a [**CRYPT\_XML\_REFERENCE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_reference) structure.</span></span><br/>          |
| <span id="CRYPT_XML_SIGNATURE_VALUE_MAX"></span><span id="crypt_xml_signature_value_max"></span><dl> <span data-ttu-id="a95b9-118"><dt>**CRYPT \_XML \_ 簽名 \_ 值 \_ 最大值**</dt> <dt>2048</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-118"><dt>**CRYPT\_XML\_SIGNATURE\_VALUE\_MAX**</dt> <dt>2048</dt></span></span> </dl> | <span data-ttu-id="a95b9-119">[**CRYPT \_ XML \_**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature)簽章結構的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a95b9-119">The maximum length, in bytes, of a [**CRYPT\_XML\_SIGNATURE**](/windows/desktop/api/Cryptxml/ns-cryptxml-crypt_xml_signature) structure.</span></span><br/>                                                                                                                         |
| <span id="CRYPT_XML_DIGEST_VALUE_MAX"></span><span id="crypt_xml_digest_value_max"></span><dl> <span data-ttu-id="a95b9-120"><dt>**CRYPT \_XML \_ 摘要 \_ 值 \_ 最大值**</dt> <dt>128</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-120"><dt>**CRYPT\_XML\_DIGEST\_VALUE\_MAX**</dt> <dt>128</dt></span></span> </dl>           | <span data-ttu-id="a95b9-121">摘要的最大長度（以位元組為單位）。</span><span class="sxs-lookup"><span data-stu-id="a95b9-121">The maximum length, in bytes, of a digest.</span></span><br/>                                                                                                                                                                                 |
| <span id="CRYPT_XML_OBJECTS_MAX"></span><span id="crypt_xml_objects_max"></span><dl> <span data-ttu-id="a95b9-122"><dt>**CRYPT \_XML \_ 物件 \_ 最大**</dt> <dt>256</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-122"><dt>**CRYPT\_XML\_OBJECTS\_MAX**</dt> <dt>256</dt></span></span> </dl>                           | <span data-ttu-id="a95b9-123">在內部使用，以指定每個簽章允許的 **物件** 元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="a95b9-123">Used internally to specify the maximum number of **Object** elements allowed per signature.</span></span><br/>                                                                                                                                |
| <span id="CRYPT_XML_REFERENCES_MAX"></span><span id="crypt_xml_references_max"></span><dl> <span data-ttu-id="a95b9-124"><dt>**CRYPT \_XML \_ 參考 \_ MAX**</dt> <dt>0x7FF8</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-124"><dt>**CRYPT\_XML\_REFERENCES\_MAX**</dt> <dt>0x7FF8</dt></span></span> </dl>               | <span data-ttu-id="a95b9-125">允許的 **參考** 元素數目上限。</span><span class="sxs-lookup"><span data-stu-id="a95b9-125">The maximum number of **Reference** elements allowed.</span></span><br/>                                                                                                                                                                      |



## <a name="requirements"></a><span data-ttu-id="a95b9-126">規格需求</span><span class="sxs-lookup"><span data-stu-id="a95b9-126">Requirements</span></span>



| <span data-ttu-id="a95b9-127">需求</span><span class="sxs-lookup"><span data-stu-id="a95b9-127">Requirement</span></span> | <span data-ttu-id="a95b9-128">值</span><span class="sxs-lookup"><span data-stu-id="a95b9-128">Value</span></span> |
|-------------------------------------|---------------------------------------------------------------------------------------|
| <span data-ttu-id="a95b9-129">最低支援的用戶端</span><span class="sxs-lookup"><span data-stu-id="a95b9-129">Minimum supported client</span></span><br/> | <span data-ttu-id="a95b9-130">\[僅限 Windows 7 桌面應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a95b9-130">Windows 7 \[desktop apps only\]</span></span><br/>                                            |
| <span data-ttu-id="a95b9-131">最低支援的伺服器</span><span class="sxs-lookup"><span data-stu-id="a95b9-131">Minimum supported server</span></span><br/> | <span data-ttu-id="a95b9-132">僅限 Windows Server 2008 R2 \[ desktop 應用程式\]</span><span class="sxs-lookup"><span data-stu-id="a95b9-132">Windows Server 2008 R2 \[desktop apps only\]</span></span><br/>                               |
| <span data-ttu-id="a95b9-133">標頭</span><span class="sxs-lookup"><span data-stu-id="a95b9-133">Header</span></span><br/>                   | <dl> <span data-ttu-id="a95b9-134"><dt>Cryptxml。h</dt></span><span class="sxs-lookup"><span data-stu-id="a95b9-134"><dt>Cryptxml.h</dt></span></span> </dl> |



 

 




