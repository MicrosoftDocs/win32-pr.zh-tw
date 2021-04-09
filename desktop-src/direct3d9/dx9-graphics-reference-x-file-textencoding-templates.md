---
description: 範本會定義資料串流的轉譯方式-資料是由範本定義來進行。 本節將討論範本的下列各方面，並提供範例範本。
ms.assetid: f84978a8-8315-4626-be68-f00f3a72e5ac
title: '範本 (X 檔案格式，文字編碼) '
ms.topic: article
ms.date: 05/31/2018
ms.openlocfilehash: 5fccec46e72a73bb5ed4434fd252595e1b072ad4
ms.sourcegitcommit: a47bd86f517de76374e4fff33cfeb613eb259a7e
ms.translationtype: MT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/06/2021
ms.locfileid: "103687372"
---
# <a name="templates-x-file-format-text-encoding"></a><span data-ttu-id="93485-104">範本 (X 檔案格式，文字編碼) </span><span class="sxs-lookup"><span data-stu-id="93485-104">Templates (X file format, text encoding)</span></span>

<span data-ttu-id="93485-105">範本會定義資料串流的轉譯方式-資料是由範本定義來進行。</span><span class="sxs-lookup"><span data-stu-id="93485-105">Templates define how the data stream is interpreted - the data is modulated by the template definition.</span></span> <span data-ttu-id="93485-106">本節將討論範本的下列各方面，並提供範例範本。</span><span class="sxs-lookup"><span data-stu-id="93485-106">This section discusses the following aspects of a template and provides an example template.</span></span>

<span data-ttu-id="93485-107">有一個特殊範本-標頭範本。</span><span class="sxs-lookup"><span data-stu-id="93485-107">There is one special template - the header template.</span></span> <span data-ttu-id="93485-108">建議每個應用程式定義標頭範本，並用它來定義應用程式特定的資訊，例如版本資訊。</span><span class="sxs-lookup"><span data-stu-id="93485-108">It is recommended that each application define a header template and use it to define application-specific information, such as version information.</span></span> <span data-ttu-id="93485-109">如果有此標頭，則會使用. x 檔案格式 API 來讀取此標頭。</span><span class="sxs-lookup"><span data-stu-id="93485-109">If present, this header is read by the .x file format API.</span></span> <span data-ttu-id="93485-110">如果有旗標成員可用，則會使用它來判斷如何解讀下列資料。</span><span class="sxs-lookup"><span data-stu-id="93485-110">If a flags member is available, it is used to determine how the following data is interpreted.</span></span> <span data-ttu-id="93485-111">旗標成員（如果已定義）應該是 DWORD。</span><span class="sxs-lookup"><span data-stu-id="93485-111">The flags member, if defined, should be a DWORD.</span></span> <span data-ttu-id="93485-112">目前已定義一個位-位0。</span><span class="sxs-lookup"><span data-stu-id="93485-112">One bit is currently defined - bit 0.</span></span> <span data-ttu-id="93485-113">如果清除此位，則檔案中的下列資料為二進位。</span><span class="sxs-lookup"><span data-stu-id="93485-113">If this bit is clear, the following data in the file is binary.</span></span> <span data-ttu-id="93485-114">如果設定，則下列資料是文字。</span><span class="sxs-lookup"><span data-stu-id="93485-114">If set, the following data is text.</span></span> <span data-ttu-id="93485-115">您可以使用多個標頭資料物件在檔案內的二進位和文字之間切換。</span><span class="sxs-lookup"><span data-stu-id="93485-115">You can use multiple header data objects to switch between binary and text within the file.</span></span>

## <a name="template-form-name-and-uuid"></a><span data-ttu-id="93485-116">範本表單、名稱和 UUID</span><span class="sxs-lookup"><span data-stu-id="93485-116">Template Form, Name, and UUID</span></span>

<span data-ttu-id="93485-117">範本的格式如下。</span><span class="sxs-lookup"><span data-stu-id="93485-117">A template has the following form.</span></span>


```
template <template-name> {
<UUID>
    <member 1>;
...
    <member n>;
[restrictions]
}
```



<span data-ttu-id="93485-118">範本名稱是英數位元名稱，可 () 包含底線字元 \_ 。</span><span class="sxs-lookup"><span data-stu-id="93485-118">The template name is an alphanumeric name that can include the underscore character (\_).</span></span> <span data-ttu-id="93485-119">不得以數位開頭。</span><span class="sxs-lookup"><span data-stu-id="93485-119">It must not begin with a digit.</span></span> <span data-ttu-id="93485-120">UUID 是一種通用的唯一識別碼，格式化為開放式 Software Foundation 的分散式運算環境標準，並以角括弧括住 (< >) 。</span><span class="sxs-lookup"><span data-stu-id="93485-120">The UUID is a universally unique identifier formatted to the Open Software Foundation's Distributed Computing Environment standard and enclosed by angle brackets (< >).</span></span> <span data-ttu-id="93485-121">例如： <3D82AB43-62DA-11cf-AB39-0020AF71E433>。</span><span class="sxs-lookup"><span data-stu-id="93485-121">For example: <3D82AB43-62DA-11cf-AB39-0020AF71E433>.</span></span>

## <a name="template-members"></a><span data-ttu-id="93485-122">範本成員</span><span class="sxs-lookup"><span data-stu-id="93485-122">Template Members</span></span>

<span data-ttu-id="93485-123">範本成員包含名為資料類型，後面接著選擇性名稱或命名資料類型的陣列。</span><span class="sxs-lookup"><span data-stu-id="93485-123">Template members consist of a named data type followed by an optional name or an array of a named data type.</span></span> <span data-ttu-id="93485-124">有效的基本資料類型定義于下表中。</span><span class="sxs-lookup"><span data-stu-id="93485-124">Valid primitive data types are defined in the following table.</span></span>



| <span data-ttu-id="93485-125">類型</span><span class="sxs-lookup"><span data-stu-id="93485-125">Type</span></span>    | <span data-ttu-id="93485-126">大小</span><span class="sxs-lookup"><span data-stu-id="93485-126">Size</span></span>                               |
|---------|------------------------------------|
| <span data-ttu-id="93485-127">WORD</span><span class="sxs-lookup"><span data-stu-id="93485-127">WORD</span></span>    | <span data-ttu-id="93485-128">16 位元</span><span class="sxs-lookup"><span data-stu-id="93485-128">16 bits</span></span>                            |
| <span data-ttu-id="93485-129">DWORD</span><span class="sxs-lookup"><span data-stu-id="93485-129">DWORD</span></span>   | <span data-ttu-id="93485-130">32 位元</span><span class="sxs-lookup"><span data-stu-id="93485-130">32 bits</span></span>                            |
| <span data-ttu-id="93485-131">FLOAT</span><span class="sxs-lookup"><span data-stu-id="93485-131">FLOAT</span></span>   | <span data-ttu-id="93485-132">IEEE float</span><span class="sxs-lookup"><span data-stu-id="93485-132">IEEE float</span></span>                         |
| <span data-ttu-id="93485-133">DOUBLE</span><span class="sxs-lookup"><span data-stu-id="93485-133">DOUBLE</span></span>  | <span data-ttu-id="93485-134">64 位元</span><span class="sxs-lookup"><span data-stu-id="93485-134">64 bits</span></span>                            |
| <span data-ttu-id="93485-135">CHAR</span><span class="sxs-lookup"><span data-stu-id="93485-135">CHAR</span></span>    | <span data-ttu-id="93485-136">8 位元</span><span class="sxs-lookup"><span data-stu-id="93485-136">8 bits</span></span>                             |
| <span data-ttu-id="93485-137">UCHAR</span><span class="sxs-lookup"><span data-stu-id="93485-137">UCHAR</span></span>   | <span data-ttu-id="93485-138">8 位元</span><span class="sxs-lookup"><span data-stu-id="93485-138">8 bits</span></span>                             |
| <span data-ttu-id="93485-139">BYTE</span><span class="sxs-lookup"><span data-stu-id="93485-139">BYTE</span></span>    | <span data-ttu-id="93485-140">8 位元</span><span class="sxs-lookup"><span data-stu-id="93485-140">8 bits</span></span>                             |
| <span data-ttu-id="93485-141">STRING</span><span class="sxs-lookup"><span data-stu-id="93485-141">STRING</span></span>  | <span data-ttu-id="93485-142">以 Null 結束的字串</span><span class="sxs-lookup"><span data-stu-id="93485-142">NULL terminated string</span></span>             |
| <span data-ttu-id="93485-143">CSTRING</span><span class="sxs-lookup"><span data-stu-id="93485-143">CSTRING</span></span> | <span data-ttu-id="93485-144"> (不支援格式化的 C 字串) </span><span class="sxs-lookup"><span data-stu-id="93485-144">Formatted C string (not supported)</span></span> |
| <span data-ttu-id="93485-145">UNICODE</span><span class="sxs-lookup"><span data-stu-id="93485-145">UNICODE</span></span> | <span data-ttu-id="93485-146">不支援 Unicode 字串 () </span><span class="sxs-lookup"><span data-stu-id="93485-146">Unicode string (not supported)</span></span>     |



 

<span data-ttu-id="93485-147">您也可以在範本定義中參考其他先前在資料流程中遇到的範本所定義的資料類型。</span><span class="sxs-lookup"><span data-stu-id="93485-147">Additional data types defined by templates encountered earlier in the data stream can also be referenced within a template definition.</span></span> <span data-ttu-id="93485-148">不允許向前參考。</span><span class="sxs-lookup"><span data-stu-id="93485-148">No forward references are allowed.</span></span>

<span data-ttu-id="93485-149">任何有效的資料類型都可以表示為範本定義中的陣列。</span><span class="sxs-lookup"><span data-stu-id="93485-149">Any valid data type can be expressed as an array in the template definition.</span></span> <span data-ttu-id="93485-150">下列範例顯示基本語法。</span><span class="sxs-lookup"><span data-stu-id="93485-150">The basic syntax is shown in the following example.</span></span>


```
array <data-type> <name>[<dimension-size>];
```



<span data-ttu-id="93485-151"><維度大小> 可以是整數，也可以是另一個樣板成員的命名參考，而該成員的值會被取代。</span><span class="sxs-lookup"><span data-stu-id="93485-151"><dimension-size> can either be an integer or a named reference to another template member whose value is then substituted.</span></span> <span data-ttu-id="93485-152">陣列可以是 n 維，其中 n 是由結尾的成對方括弧數目所決定，如下列範例所示。</span><span class="sxs-lookup"><span data-stu-id="93485-152">Arrays can be n-dimensional, where n is determined by the number of paired square brackets trailing the statement, as in the following example.</span></span>


```
array DWORD FixedHerd[24];
array DWORD Herd[nCows];
array FLOAT Matrix4x4[4][4];
```



## <a name="template-restrictions"></a><span data-ttu-id="93485-153">範本限制</span><span class="sxs-lookup"><span data-stu-id="93485-153">Template Restrictions</span></span>

<span data-ttu-id="93485-154">範本可以是開啟、關閉或限制的。</span><span class="sxs-lookup"><span data-stu-id="93485-154">Templates can be open, closed, or restricted.</span></span> <span data-ttu-id="93485-155">這些限制會決定哪些資料類型可以出現在範本所定義之資料物件的直屬階層中。</span><span class="sxs-lookup"><span data-stu-id="93485-155">These restrictions determine which data types can appear in the immediate hierarchy of a data object defined by the template.</span></span> <span data-ttu-id="93485-156">開啟的範本沒有任何限制，關閉的範本會拒絕所有的資料類型，且受限制的範本允許資料類型的名稱清單。</span><span class="sxs-lookup"><span data-stu-id="93485-156">An open template has no restrictions, a closed template rejects all data types, and a restricted template allows a named list of data types.</span></span>

<span data-ttu-id="93485-157">指出開啟範本的語法是以方括弧括住的三個句點。</span><span class="sxs-lookup"><span data-stu-id="93485-157">The syntax for indicating an open template is three periods enclosed by square brackets.</span></span>


```
[ ... ]
```



<span data-ttu-id="93485-158">以逗號分隔的已命名資料類型清單，並以方括弧括住的 Uuid （以方括弧括住）表示受限的範本。</span><span class="sxs-lookup"><span data-stu-id="93485-158">A comma-separated list of named data types followed optionally by their UUIDs enclosed by square brackets indicates a restricted template.</span></span>


```
[ { data-type [ UUID ] , } ... ]
```



<span data-ttu-id="93485-159">上述任一項都沒有指出已關閉的範本。</span><span class="sxs-lookup"><span data-stu-id="93485-159">The absence of either of the above indicates a closed template.</span></span>

## <a name="template-example"></a><span data-ttu-id="93485-160">範本範例</span><span class="sxs-lookup"><span data-stu-id="93485-160">Template Example</span></span>

<span data-ttu-id="93485-161">以下顯示範例範本。</span><span class="sxs-lookup"><span data-stu-id="93485-161">The following shows an example template.</span></span>


```
template Mesh {
<3D82AB44-62DA-11cf-AB39-0020AF71E433>
DWORD nVertices;
array Vector vertices[nVertices];
DWORD nFaces;
array MeshFace faces[nFaces];
 [ ... ]                // An open template
}
template Vector {
<3D82AB5E-62DA-11cf-AB39-0020AF71E433>
FLOAT x;
FLOAT y;
FLOAT z;
}                        // A closed template
template FileSystem {
<UUID>
STRING name;
[ Directory <UUID>, File <UUID> ]    // A restricted template
}
```



## <a name="related-topics"></a><span data-ttu-id="93485-162">相關主題</span><span class="sxs-lookup"><span data-stu-id="93485-162">Related topics</span></span>

<dl> <dt>

[<span data-ttu-id="93485-163">文字編碼方式</span><span class="sxs-lookup"><span data-stu-id="93485-163">Text Encoding</span></span>](text-encoding.md)
</dt> </dl>

 

 



